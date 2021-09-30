**Kotlin Flow**

**Data types** \
Everything is an Object( can have member functions ). Primitives at runtime but Objects to user.

**Keywords** \
*internal* - Setting a declaration as internal means that it'll be available in the same module only.

**Local Functions** - **A function inside a funtion.** \
A private function (used only by a single calling method) can be used as local functions when we need local variables in the calling function without passing it.

**For Example:**
        
        fun countRangeSum(nums: IntArray, lower: Int, upper: Int): Int {
          var count = 0
          //process nums array and call. value of sum is computed which is omitted for simplicity. 
          if(isValidRangeSum(sum, lower, upper)} { count++ }
        }

        private fun isValidRangeSum( sum : Int, lower : Int, upper : Int) = (rangeSum >= lower && rangeSum <= upper)

**If implemented as Local function:**
        
        fun countRangeSum(nums: IntArray, lower: Int, upper: Int): Int {
            var count = 0
        
            fun ifValidRangeSumUpdateCount( sum : Int){
              if(rangeSum >= lower && rangeSum <= upper) { count++ }
            }
        
            //process nums array and call. value of sum is computed which is omitted for simplicity. 
            ifValidRangeSumUpdateCount(sum)
        }

**Advantage:**
1. No need to pass local variables for computation.
2. Can update values of primitive data types directly. As primitives as call by value and not call by reference.
    
    




        
        
