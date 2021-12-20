Circle Area
function area(diameter){
console.log(3.14(diameter*diameter));
}

//area(4);



POST SIRALAMA İŞLEMLERİ
let post = [
  { name: "Post1", description: "Post1" },
  { name: "Post2", description: "Post2" },
  { name: "Post3", description: "Post3" },
  { name: "Post4", description: "Post4" },
  { name: "Post5", description: "Post5" },
];

function postSirala(val) {
  val.forEach((item) => {
    console.log(`Postun adı ${item.name} açıklaması ise ${item.description}`);
  });
}

function postEkle(obj) {
  const promise1 = new Promise((resolve, reject) => {
    setTimeout(() => {
      post.push(obj);
      resolve(post);
      reject("Bir hata oluştu");
    }, 5000);
  });
  return promise1;
}

async function islem() {
  await postEkle({ name: "Post6", description: "Post6" });
  postSirala(post);
}

islem();
