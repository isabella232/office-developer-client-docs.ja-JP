---
title: TNEF ストリーム構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e77c043e4f152740af9bdb2b8fb5b7bedece1c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430204"
---
# <a name="tnef-stream-structure"></a>TNEF ストリーム構造

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
TNEF ストリームは、ストリームを TNEF ストリームとして識別する 32 ビットの署名で始まります。 署名に続く 16 ビット符号なし整数は、タグ付きメッセージ テキスト内の添付ファイルの場所を相互参照するキーとして使用されます。 ストリームの残りの部分は、TNEF 属性のシーケンスです。 メッセージ属性は TNEF ストリームの最初に表示され、添付ファイルの属性が続きます。 特定の添付ファイルに属する属性は **、attAttachRenddata** 属性で始まるグループ化されます。 
  
TNEF ストリームで使用される定数値の大部分は、TNEF で定義されます。H ヘッダー ファイル。 特に **、TNEF_SIGNATURE** **、LVL_MESSAGE、LVL_ATTACHMENT、** およびすべてのTNEF 属性識別子がこのファイルで定義されています。 他の定数には、C 言語コンパイラに対する解釈によって示される値があります。 通常、このような定数は、次の項目のサイズを指定するために使用されます。 たとえば、 **アイテム定義の sizeof(ULONG)** は、TNEF ストリーム内のその場所で、次の符号なし長整数のサイズを表す整数が発生する必要があります。 
  
TNEF ストリーム内のすべての整数は、リトル エンディアン バイナリ形式で格納されますが、このセクション全体を 16 進数で示します。 チェックサム値は、チェックサムが適用されるデータのバイトの合計である 65536 の 16 ビット符号なし整数です。 すべての属性の長さは、終端の null 文字を含む符号なし長整数です。
  
キーは、添付ファイル参照キーの初期値を表す 0 以外の 16 ビット符号なし整数です。 添付ファイル参照キーは、TNEF を使用しているサービス プロバイダーによって [OpenTnefStream](opentnefstream.md) 関数に渡される初期値で順番に各添付ファイルに割り当てられます。 サービス プロバイダーは、2 つのメッセージが同じキーを使用する可能性を最小限に抑えるために、キーの初期値をランダムに生成する必要があります。 
  
TNEF 実装では、属性識別子を使用して属性を対応する MAPI プロパティにマップします。 属性識別子は、2 つの単語値で作られた 32 ビットの符号なし整数です。 高次単語は、文字列やバイナリなどのデータ型を示し、低次単語は特定の属性を識別します。 高次ワードのデータ型は次のとおりです。
  
|**Type**|**値**|
|:-----|:-----|
|atpTriples  <br/> |0x0000  <br/> |
|atpString  <br/> |0x0001  <br/> |
|atpText  <br/> |0x0002  <br/> |
|atpDate  <br/> |0x0003  <br/> |
|atpShort  <br/> |0x0004  <br/> |
|atpLong  <br/> |0x0005  <br/> |
|atpByte  <br/> |0x0006  <br/> |
|atpWord  <br/> |0x0007  <br/> |
|atpDword  <br/> |0x0008  <br/> |
|atpMax  <br/> |0x0009  <br/> |
   
各属性の低次ワード値は、TNEF で定義されます。H ヘッダー ファイル。
  

