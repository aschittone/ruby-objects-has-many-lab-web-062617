class Furniture
	attr_accessor :name, :room, :house

	def initialize(name, room)
		@name = name
		@room = room
	end

	def house_name
		self.house.name
	end
end

class House
	attr_accessor :address, :room

	def initialize(name)
		@name = name
		@furniture = []
	end

	def add_furniture_by_name(name, room)
		furniture = Furniture.new(name, room)
		@furniture << furniture
		furniture.house = self
	end

	def furniture 
		@furniture
	end
	
	def get_furniture(room_choice)
	  self.furniture.select do |piece_of_furniture| 
	    if piece_of_furniture.room == room_choice 
	      puts piece_of_furniture.name
	    end
	  end
	end
end

house = House.new("Laurens New House")
house.add_furniture_by_name("couch", "living room")
house.add_furniture_by_name("table", "kitchen")
