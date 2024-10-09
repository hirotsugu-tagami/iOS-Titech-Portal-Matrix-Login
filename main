// A1,A2,... カンマは抜いてください
data = "xxx……";

//マトリクスの座標ゲット
let tmpo = document.getElementsByTagName('tr');
   for(let i = 0; i<tmpo.length;i++) {
       console.log(i + ":" + tmpo.item(i).textContent)
      }

//英字を数字へ変換
function alphabet2int(str) {
     const alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
     return alphabet.indexOf(str);
    }
    
// 英字を見つける
function findEng(tmp) {
   for(let i = 0; i < tmp.length; i++) {
        if(alphabet2int(tmp[i]) !== -1) {
            return i;
       }
    }
    return 0;
}

//dataのIndex番号計算
//英字の番号(0始まり)*7+(数字-1)
//例：D5 なら，3*7 + (5-1) = 25
function getIndexNum(tmp) {
    let engIndex = findEng(tmp)
    let eng = alphabet2int(tmp[engIndex]);
    let num = tmp[engIndex+2]
    //英字を数字へ変換
    let len = eng * 7;
    let row = num - 1;
    return len + row;
 
}

//引数は4,5,6
let codenum = [5, 6, 7]
  for(let i = 0; i<3; i++) {
      document.getElementsByName("message" + (i+3).toString()).item(0).value = data[getIndexNum(tmpo.item(codenum[i]).textContent)];
  }

//OKをクリック
document.getElementsByName("OK").item(0).click();

// completionを呼び出して終了
completion();
