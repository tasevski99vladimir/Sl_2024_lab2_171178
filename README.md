Vladimir Tasevski 171178

2. CFG

     [1] Start
    |
  [2] Check allItems null?
    |-- (true) --> [Exception: "allItems list can't be null!"]
    |-- (false) --> [3]
  [3] Initialize total
    |
  [4] For each item in allItems
    |-- (empty) --> [13]
    |-- (not empty) --> [5]
  [5] Check item name
    |-- (true) --> [Set name to "unknown"]
    |-- (false) --> [6]
  [6] Check item barcode null?
    |-- (true) --> [Exception: "No barcode!"]
    |-- (false) --> [7]
  [7] Validate barcode
    |-- (false) --> [Exception: "Invalid character in item barcode!"]
    |-- (true) --> [8]
  [8] Calculate item price
    |
  [9] Apply discount?
    |-- (true) --> [Apply discount]
    |-- (false) --> [10]
  [10] Additional discount check?
    |-- (true) --> [Apply additional discount]
    |-- (false) --> [11]
  [11] Update total
    |
  [12] Loop end
    |-- (more items) --> [5]
    |-- (no more items) --> [13]
  [13] Final check
    |-- (true) --> [Return true]
    |-- (false) --> [Return false]
  [14] End
