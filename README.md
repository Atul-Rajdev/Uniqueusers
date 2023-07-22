# listofuser.js

function getUniqueUsersNotInList2(list1, list2) {
  const set1 = new Set(list1);
  const set2 = new Set(list2);
  const uniqueUsersNotInList2 = new Set([...set1].filter(user => !set2.has(user)));
  return Array.from(uniqueUsersNotInList2);
}

function getUniqueUsersNotInList1(list1, list2) {
  const set1 = new Set(list1);
  const set2 = new Set(list2);
  const uniqueUsersNotInList1 = new Set([...set2].filter(user => !set1.has(user)));
  return Array.from(uniqueUsersNotInList1);
}

function getIntersectionOfLists(list1, list2) {
  const set1 = new Set(list1);
  const set2 = new Set(list2);
  const intersection = new Set([...set1].filter(user => set2.has(user)));
  return Array.from(intersection);
}


const List1 = ['Arjun', 'Adwait', 'Swapnil', 'Amit', 'Vishal', 'Adnan'];
const List2 = ['Adwait', 'Laxman', 'Amit', 'Adnan', 'Nitin', 'Gourav'];


const uniqueUsersNotInList2 = getUniqueUsersNotInList2(List1, List2);
console.log("Unique users from List1 not in List2:", uniqueUsersNotInList2);

const uniqueUsersNotInList1 = getUniqueUsersNotInList1(List1, List2);
console.log("Unique users from List2 not in List1:", uniqueUsersNotInList1);


const intersectionOfLists = getIntersectionOfLists(List1, List2);
console.log("Users present in both List1 and List2:", intersectionOfLists);
