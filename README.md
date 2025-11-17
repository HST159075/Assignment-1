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
