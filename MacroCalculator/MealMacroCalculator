#include <iostream>
#include <string>
#include <vector>

int main() {
	class ingredient {
	public:
		int weightAmount;
		double protein;
		double fat;
		double carbs;
	};

	class Meal {
	public:
		double totalWeight;
		double totalProtein;
		double totalFat;
		double totalCarbs;

		bool highProtein;
		bool lowFat;
		bool lowCarbs;
	};

	int ingredientAmount;

	std::cout << "First enter the amount of ingredients in the meal then enter the weight (in grams) of the ingredientin the meal then the amount of protein, fat & carbs in 100g of the ingredient. \n";

	std::cout << "Enter amount of ingredients: ";
	std::cin >> ingredientAmount;

	ingredient ingredients;

	Meal meal{0, 0, 0, 0, false, false, false};

	for (int i = 0; i < ingredientAmount; i++) {
		
		std::cout << "Enter ingredient weight: ";
		std::cin >> ingredients.weightAmount;
		meal.totalWeight += ingredients.weightAmount;
		double Timer = ingredients.weightAmount / 100;

		std::cout << "Enter ingredient protein: ";
		std::cin >> ingredients.protein;
		meal.totalProtein += (ingredients.protein * Timer);

		std::cout << "Enter ingredient fat: ";
		std::cin >> ingredients.fat;
		meal.totalFat += (ingredients.fat * Timer);

		std::cout << "Enter ingredient carbs: ";
		std::cin >> ingredients.carbs;
		meal.totalCarbs += (ingredients.carbs * Timer);
	}

	meal.highProtein = ((meal.totalProtein / meal.totalWeight) >= .30 ? true : false);
	meal.lowFat = ((meal.totalFat / meal.totalWeight) <= .05 ? true : false);
	meal.lowCarbs = ((meal.totalCarbs / meal.totalWeight) <= 3 ? true : false);

	if (meal.highProtein) { std::cout << "The Meal is High in Protein \n"; }
	else { std::cout << "The Meal isn't high in Protein \n"; }

	if (meal.lowFat) { std::cout << "The Meal is Low in Fat \n"; }
	else { std::cout << "The Meal isn't Low in Fat \n"; }

	if (meal.highProtein) { std::cout << "The Meal is High in Carbs \n"; }
	else { std::cout << "The Meal isn't low in Carbs \n"; }

	return 0;
}
