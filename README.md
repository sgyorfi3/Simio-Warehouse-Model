# Simio-Warehouse-Model
For this assignment, I was tasked with recreating a Warehouse using Simio and then recommending changes to improve its performance.

Assignment Instruction:

A local warehouse has been contracted by one of the big eCommerce companies to provide better service to local customers. The warehouse has eight diﬀerent areas for the types of products they store (and would ultimately pick to send to customers): Electronics (EL), Jewelry (JY), Beauty & Bath (BB), Cookware (CK), Sporting Goods (SG), Toys (TY), Pet Supplies (PS), and Tools (TO).

When an order comes in, an employee (picker) will be assigned to that order and would travel through the warehouse to pick the items for the order. Once the picker has all of the items, he will take it to a shipping area where the items are appropriately boxed, and the whole order inspected. Once the order passes inspection, the picker is done with the order and can then start the next order, and the just-ﬁnished-order goes to the loading dock to be put on a truck for delivery. The client has a separate team working with the loading dock system, so you will assume that this system ends when the order passes inspection.

There are currently 4 pickers working and they work the full eight hours without a break (I know, that violates labor law, but this is a project after all). There is one manager working the full eight hours too. The inspection process takes Tria(1,3,6) minutes and there is a 10% probability that the picked order fails inspection (employee training could reduce this to 7%). When that occurs, the picker will go back to the random area to return the wrong item, pick the right item, and then allow that order to leave the system (to the loading dock); we are assuming that the corrected order will not need to be re-inspected. Additionally, if inspection fails, there will be one (and only one) area to return with any area being equally likely (in other words, randomly select one area to return to).

Orders arrive according to an Exponential distribution on average every 8 minutes. The orders can be characterized as “small” (a few items spread around the areas) or “large” (most of the items need to be picked). Small orders comprise 65% of all orders. Table 1 lists, by order size, the probability that order will contain at least one item from that area. Do not worry about the quantity of an item to pick, but rather assume that picking more than one would not add measurable time. The order should be determined when it arrives. Notice that it is possible for a Small order to include an item from each area (but a small probability) or for either order type to not have an item to pick (again, a small probability and if that happens, consider it a blessing as it can help our statistics).

Most of the areas have enough space to accommodate three pickers at the same time, but Tools and Cookware can only accommodate two pickers at the same time; right now, if an area is full, a new picker arriving will just have to wait his turn. Additionally, because Electronics and Jewelry items have high value, they are securely locked and the one manager working has to validate the order and oversee the pick (you can assume the manager’s time has been included in the pick time distributions). Table 2 lists the distributions for the random amount of time to pick for the order in that area (if that area is included on the order); “T” represents Triangular and “U” represents Uniform, the units are all in minutes, and remember that time is continuous.

The warehouse layout is as shown in Figure 1; consider the border to be the walls and the shelves are labeled A through H. It would be too expensive to re-arrange the shelving, but you could re-arrange where the items for each area are stored (that is not as expensive but there should be a good reason to justify that expense). For example, you can’t put the shelves into a star pattern, but you could swap where Toys and Sporting Goods are stored. Also notice
that if you swap locations with Tools or Cookware, the space limitation will apply to those newly-placed items. You may use your best judgment on the physical distances; try to be realistic, but do not spend too much time on this (but they should still be in these general locations). You may also select if you want pickers to be able to randomly visit the areas in any order (provided they visit each one they need to) or if you want them to follow a speciﬁc path through the warehouse (some warehouses do this in order to minimize the chance of a collision). If you let pickers go to any area willy-nilly, then you’ll need logic to ensure they visit the right areas. If you make pickers follow a speciﬁc path, you’ll have to accommodate being able to skip through an area if they don’t need to visit that area. For example, an order may only include Cookware, so whichever method you choose, the picker should not have to wait or spend time in any area other than Cookware.

The simulation should be run for 8 hours and no warm-up is necessary, but any orders still in the system should be allowed to complete. The client has a 95% service level agreement that all orders will be picked and to shipping within 30 minutes. In other words, 95% of orders
should be processed (through this system) in 30 minutes or less. You should determine ﬁrst if the service level agreement is currently met and if not, what change(s) can be inexpensively made to meet it; if it is being met, determine what changes could be made to reduce costs. Like all good managers, the client would also like to keep costs low by using the least amount of employees possible.

Remember you are looking for two reasonable changes to make to the system to ensure that the service level agreement is met at the lowest cost. It is acceptable if a reasonable change does not result in an improvement.

