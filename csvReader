# As input, it utilizes a .cvs document with three columns: Zone, Parking space num., and available spaces
# It returns the number of occupied spaces in each zone and their average

# In case columns are in another order, this variables mus be changed to accomodate that
avlb = 2
zone = 0

values = []
diff = 1
with open('Estacionamiento.csv', 'r') as csv:
    for line in csv.readlines():
        elements = line.strip().split(',')
        if diff != int(elements[zone]):
            csum = sum(values)
            cavg = sum(values)/len(values)
            print("Occupied spaces on zone %d: %d" % (diff, csum))
            print("Average of occupied spaces on zone %d: %f" % (diff, cavg))
            print()
            values = []
            diff = int(elements[zone])
        values.append(int(elements[avlb]))

csum = sum(values)
cavg = sum(values)/len(values)
print("Occupied spaces on zone %d: %d" % (diff, csum))
print("Average of occupied spaces on zone %d: %f" % (diff, cavg))
