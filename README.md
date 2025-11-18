# Assignment-1

  ২ নং প্রশ্নের উত্তর

TypeScript-এর keyof হলো একটি type operator ।
কোনো object type-এর ওপর keyof ব্যবহার করলে, সেই object type-এর সকল property নামকে নিয়ে একটি union টাইপ তৈরি করে।
অর্থাৎ object-এর যে property গুলো আছে—keyof সেগুলোর নামগুলোকে টাইপ হিসেবে রিটার্ন দেয়।

উদাহরণ:
interface User {
  id: number;
  name: string;
}

function getProperty(obj: User, key: keyof User) {
  return obj[key];
}

const user: User = {
  id: 102,
  name: "Tasin"
};


   3 নং প্রশ্নের উত্তর

Any-
any টাইপ ব্যাবহার করলে, আমরা TypeScript এর ভ্যারিয়েবল এর সাথে যেকোনো কিছু করতে পারি,
কোন Error দেব না। TypeScript কোনো টাইপ চেক করে না।

Unknown -
unknown টাইপ এ যেকোনো কিছু স্টোর করা যাবে। স্টোর করার আগে অবশ্যই টাইপ চেক করতে হবে, না হয় error আসবে।

ঝংকর মাহবুব স্যার এর সহজ কথায় :
 Any মানে >> TypeScript আরে কিছু হইতোনো, আর মনত  যিয়েন আইয়ি -ইয়েন লিকুম।
 Unknown মানে >> তুই যা খুশি স্টোর গর, কিন্তু ব্যাবহার গরিবের আগে চেক দেহ, না হলে গরম মাইয়া হয়ে যাইবো।

Never -
Never-টাইপ হলো এমন একটি টাইপ যা আমাকে কখনো কিছু দিতে পারবে না বা  return করবে না।
এটা সাধারনত ব্যবহার হয়, সাধারণ ফাংশনে যা exception throw করে বা অনন্ত লুপে চলে।
