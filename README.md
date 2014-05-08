VehicleJ
========
*
 * To change this template, choose Tools | Templates
 * and open the template in the editor.
 */
package fuelpurchase;

/**
 *
 * @author 041209329
 */
package fuelpurchase;

/**
 *
 * @author 041209329
 */
public class Vehicle {

   
	private String			manufacturer;
	private String			model;
	private int			makeYear;
        private Journey			journey;

	@SuppressWarnings("unused")
	private FuelPurchase	fuelPurchase;

	/**
	 * Class constructor
	 */
	public Vehicle() {
		this.manufacturer = "Central";
		this.model = "ITWEB";
		this.makeYear = 2014;
		journey = new Journey();
		fuelPurchase = new FuelPurchase(125.6);
	}

	/**
	 * Class constructor specifying name of manufacturer, name of model and year
	 * of make.
	 * 
	 * @param manufacturer
	 * @param model
	 * @param makeYear
	 */
	public Vehicle(String manufacturer, String model, int makeYear) {
		this.manufacturer = manufacturer;
		this.model = model;
		this.makeYear = makeYear;
		journey = new Journey();
		fuelPurchase = new FuelPurchase(125.6);
	}

	/**
	 * Prints details for {@link Vehicle}
	 */
	public void printDetails() {
		
                System.out.println("Manufacturer: " + (" Manufactured by ") + manufacturer);
		System.out.println("Car Model: " + (" Model ") + model);
		System.out.println("Year of Production: " + (" Year ") + makeYear);
                System.out.println("The Total Distance Travelled in Kilometers: " + journey.getKilometers() + " Kilometers ");
		System.out.println("Services Undergone: " + journey.getTotalServices() + " Services was Undergone ");
                System.out.println("This vehicle achieve a fuel consumption of: " + journey.getFuel() + " Litres per 100km ");
	}

	/**
	 * Appends the distance parameter to {@link Journey#getKilometers()}
	 * 
	 * @param distance
	 *            distance of kilometers traveled
	 */
	
        public void addKilometers(double distance) {
		journey.addKilometers(distance);
	}

}
