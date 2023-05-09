# genAccountFromText
generate accounts json from pay list

レシート等をテキストファイルに入力
テキストファイルを勘定に変換
変換には勘定名のテンプレートを使用する


交通費を自動生成
支払い場所までの交通費リストを作り、電車代金を自動生成
同日日に複数の支払い項目がある場合、最遠のものを1つ追加する

テキストファイルは場所単位で作成し、ファイル名末尾に場所を記述し、ファイル名から交通費を取得する
ファイル名の先頭は勘定名とし、対応する相手勘定はテンプレートから取得する
>>>値をテンプレートにいれるイメージか


テキストファイルはシンプルに記述
m/d price
m/d price memo
m/d selector price memo
など、項目ごとにシンプルに入力できるようにする


//---
webからdownlowdするファイル
銀行等のwebからDLするcsv,pdfも勘定化する
pdfは別途テキストファイルに変換してからコンバートする


//----
勘定化したjsonファイルは別途集計アプリで全勘定を生成し、
残高試算表の元データをする


//----
データは
2023/recipetフォルダにレシートテキスト
2023/statementフォルダにダウンロードファイル
を設定する


//----
templateはjsonにまとめるのか、それぞれのデータファイルに記述するのか。
データファイルに書いてしまうのも解りやすいかもしれない



//-----
データから自動生成する交通費勘定はどうするか。
いったん該当データ(外出時に発生しているレシートから生成)から生成し、
日にちが重なるものは最遠のもののみセレクトする



