using System;
using System.Collections.Generic;				
public class RTSLabsSolution
{
	public static void Main()
	{

		//testing stringRotation
		string original = "MyString";
		int rotationValue = 2;
		
		string result = stringRotation(original, rotationValue);

		Console.WriteLine("Rotating {0} characters in the String '{1}' results in: '{2}'",rotationValue, original, result);

		
		//testing aboveBelow
		List<int> collection = new List<int>{1, 5, 2, 1, 10};
	 	Dictionary<string, int> response = aboveBelow(collection, 6);
		
		
		Console.WriteLine("Above : {0} Below : {1}", response["above"].ToString(), response["below"].ToString());
	
	}
	
	
	//note, under this design spec numbers equal to the comparator won't be included in either bucket		
	public static Dictionary<string, int> aboveBelow(List<int> collection, int comparator)
	{
        	int above = 0;
			int below = 0;

		foreach(var item in collection)
		{
			if (item > comparator)
				above++;
			if (item < comparator)
				below++;
		}
		
		
		
		var comparedDictionary = new Dictionary<string, int>();		
		
		comparedDictionary.Add("above", above);
		comparedDictionary.Add("below", below);
		return comparedDictionary;
	}

	
	public static string stringRotation(string original, int rotationValue)
	{
			
	
		// added to handle the case where the rotationvalue is greater than the original strings length- 
		// a full rotation is the equivilant of NO rotation, so we just take teh modulus instead
		rotationValue = rotationValue % original.Length;	
		
		//added to handle negative rotations. Allows the user to rotate both ways!
		if(rotationValue < 0)
		rotationValue = rotationValue + original.Length;

		Console.WriteLine(rotationValue);

		
        var res = original.Substring(original.Length - rotationValue, rotationValue) + original.Substring(0, original.Length - rotationValue);
        return res;

	}

}



