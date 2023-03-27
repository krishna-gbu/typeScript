# typeScript

console.log('hello world');
let age: number = 20;
if (age<50) {
    age +=10
}
console.log(age);

let sales: number = 123;
let course: string = "dflkdsj";
let is_publised: boolean = true;

let level;
level = 10;
level = "a";

function render(doc: any) {
  console.log(doc);
}

// /array//

let number = [1, 2, 2, "2"];
let no: number[] = [1, 12, 3];
no.forEach((n) => console.log(n.toLocaleString()));

/////// tuple ////
let user: [number, string, Number[]] = [1, "krishna", [1, 2, 4]];
user[1];

///enums//
const small = 1;
const medium = 2;
const large = 3;

enum Size {
  small = 1,
  medium,
  large,
}
enum Size {
  l = 1,
  m,
  e,
}
console.log(Size.l);

// functions

function calculateTax(income: number): number {
  if (income < 50000) {
     return income * 1.2;
  }
  return income * 1.3;
}

// / default parameters
function calculateTax2(income: number,tax=2022) {
  if (tax < 2022) {
     return income * 1.2;
  }
   income * 1.3;
}

console.log(calculateTax2(5000))

let employee2:{
    id: number,
    name?:string,
    retire:(date:Date)=>void
} =
 {
   id:22,
   retire:(data:Date)=> {console.log(data)}
}

console.log(employee2.retire(new Date()));

// / type aliase

type Employee={
  readonly id:number,
   name:string
}

let employee:Employee ={id:1,name:'krish'}

console.log(employee);

// / union types

function kgToLbs(weight:number|string):number{
   if(typeof weight === 'number')
      return weight * 5
   else
      return parseInt(weight) * 10
}

console.log(kgToLbs(10));
console.log(kgToLbs('10kg'))

// literal type

type Quentity = 30|40
let quantity:Quentity = 40

console.log(quantity);

type Metric = 'cm' | 'inch'

let metric:Metric = 'inch'
console.log(metric);

// optional chaning////

type Customer = {
  birthday: Date;
};

 function getCustomer(id: number): Customer | null | undefined {
  return id === 0 ? null : { birthday: new Date() };
}

console.log(getCustomer(0)?.birthday);
console.log(getCustomer(1)?.birthday);


let log: any = null
log?.('a')


let pay:(6000|10000)=6000
console.log(pay);
