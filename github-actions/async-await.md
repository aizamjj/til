# Using async/await with Mongoose

After trying to debug why I was getting an undefined for restaurant, I realized I was not returning the result of the database query.

*controller.js*

    const getRestaurant = async (req, res) => {
        try { 
          const { id } = req.params;
          const restaurant = await models.getRestaurantById(id);
          res.send(restaurant);
        } catch (error) {
          console.error(error.stack);
          res.status(500).send([]);
        }
    }

*model.js*

    const getRestaurantById = (id) => {
        return Restaurant.findById(id).exec();
    }

