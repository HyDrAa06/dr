### Console.WriteLine("Flower type: ");
string type=Console.ReadLine();

int br, budget;
double totalPrice=0;

Console.WriteLine("Flower amount: ");
br = int.Parse(Console.ReadLine());


if (br < 10 || br > 1000)
{
	throw new ArgumentException("Invalid amount");
}

Console.WriteLine("Budget: ");
budget = int.Parse(Console.ReadLine());

if (budget < 50 || budget > 2500)
{
	throw new ArgumentException("Invalid budget");
}

string result = string.Empty;

switch(type)
{
	case "Roses":
		
		
		{
			totalPrice = br * 5;

			if (br > 80)
			{

				totalPrice *= 0.9;
			}

			break;
		}

	case "Dahlias":

		{
			totalPrice = br * 3.8;

			if (br > 90)
			{
				totalPrice *= 0.85;
			}
			
			break;
			
		}


}

if (budget >= totalPrice)
{
	double Rest = budget - totalPrice;
	Console.WriteLine("Hey, you have a great garden with " + br + " " + type + " and " + Rest + " leva left.");
}

else
{
	double expense = totalPrice - budget;
	Console.WriteLine("Not enough money, you need " + expense + " leva more.");
}



//finish for hw
Console.ReadLine();
