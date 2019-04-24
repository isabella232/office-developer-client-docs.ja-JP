---
title: TNEF ストリームの構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e77c043e4f152740af9bdb2b8fb5b7bedece1c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327385"
---
# <a name="tnef-stream-structure"></a>TNEF ストリームの構造

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
tnef ストリームは、tnef ストリームとしてストリームを識別する32ビットの署名で始まります。 このシグネチャは16ビットの符号なし整数で、タグ付きメッセージテキスト内の場所への添付ファイルを相互参照するためのキーとして使用されます。 ストリームの残りの部分は、TNEF 属性のシーケンスです。 メッセージ属性は TNEF ストリームの最初に表示され、添付ファイル属性は次のようになります。 特定の添付ファイルに属する属性は、 **attAttachRenddata**属性で始まるグループにまとめられています。 
  
tnef ストリームで使用される定数値のほとんどは、tnef で定義されています。H ヘッダーファイル。 特に、このファイルでは、 **TNEF_SIGNATURE**、 **LVL_MESSAGE**、 **LVL_ATTACHMENT**、およびすべての TNEF 属性識別子が定義されています。 他の定数には、C 言語コンパイラに対する解釈によって示される値があります。 通常、このような定数は、次の項目のサイズを指定するために使用されます。 たとえば、アイテムの定義内の**sizeof (ULONG)** は、TNEF ストリーム内のその場所で、次の符号なし長整数のサイズを表す整数が発生することを示しています。 
  
TNEF ストリーム内のすべての整数は、リトルエンディアンバイナリ形式で格納されますが、このセクション全体で16進数で表示されます。 チェックサムの値は、チェックサムが適用されるデータのバイト数の合計 (モジュロ 65536) である16ビットの符号なし整数です。 すべての属性の長さは、終端の null 文字を含む、符号なしの long 整数です。
  
キーは、添付ファイル参照キーの初期値を示す、0以外の16ビット符号なし整数です。 添付ファイルの参照キーは、TNEF を使用しているサービスプロバイダーによって[OpenTnefStream](opentnefstream.md)関数に渡される初期値から順に、各添付ファイルに割り当てられます。 サービスプロバイダーは、2つのメッセージが同じキーを使用する可能性を最小限にするために、キーのランダムな初期値を生成する必要があります。 
  
TNEF 実装は、属性識別子を使用して、対応する MAPI プロパティに属性をマップします。 属性識別子は、2つの単語値で構成される32ビットの符号なし整数です。 上位の単語は、文字列やバイナリなどのデータ型を示し、下位の単語は特定の属性を識別します。 上位の単語のデータ型は次のとおりです。
  
|**Type**|**値**|
|:-----|:-----|
|atpTriples  <br/> |0x0000  <br/> |
|atpstring  <br/> |0x0001  <br/> |
|atptext  <br/> |0x0002  <br/> |
|atpDate  <br/> |0x0003  <br/> |
|atpshort  <br/> |0x0004  <br/> |
|atpltar  <br/> |0x0005  <br/> |
|atpbyte  <br/> |0x0006  <br/> |
|atpword  <br/> |0x0007  <br/> |
|atpdword  <br/> |0x0008  <br/> |
|atpmax  <br/> |0x0009  <br/> |
   
各属性の下位ワード値は、TNEF で定義されています。H ヘッダーファイル。
  

