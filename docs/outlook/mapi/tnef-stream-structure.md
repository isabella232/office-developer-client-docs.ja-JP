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
ms.openlocfilehash: 0fcd1c79d1c0debfb18d270dc0e40de42842c6d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804123"
---
# <a name="tnef-stream-structure"></a>TNEF ストリームの構造

  
  
**適用対象**: Outlook 
  
TNEF ストリームは、TNEF ストリームとストリームを識別する 32 ビットの署名で開始します。 次の署名は、タグ付けされたメッセージのテキスト内の位置に添付ファイルを相互参照するキーとして使用される 16 ビットの符号なし整数です。 ストリームの残りの部分は、TNEF の属性のシーケンスです。 TNEF ストリームで指定されたメッセージの属性が先頭に表示され、添付ファイルの属性に従います。 特定の添付ファイルに属している属性グループ化、 **attAttachRenddata**属性を使用して開始します。 
  
TNEF ストリームで使用されている定数の値のほとんどは、TNEF で定義されます。H ヘッダー ファイルです。 特に、 **TNEF_SIGNATURE**、 **LVL_MESSAGE**、 **LVL_ATTACHMENT**、およびすべての TNEF 属性識別子は、このファイルで定義されます。 C 言語コンパイラの解釈によって示される値は、他の定数であります。 通常、このような定数を使用して次の項目のサイズを指定します。 たとえば、項目の定義では、 **sizeof(ULONG)** では、TNEF ストリーム内の場所に次の符号なし長整数型のサイズを表す整数値が発生することを示します。 
  
TNEF ストリーム内のすべての整数はリトル エンディアンの 2 進形式で格納されますが、このセクション全体で 16 進数で表示されます。 チェックサムの値は、合計、65536、チェックサムが適用されるデータのバイト数の剰余は、単に 16 ビットの符号なし整数です。 すべての属性の長さは、終端の null 文字を含む、符号なし長整数です。
  
キーは、添付ファイルの参照キーの初期値を示す 0 以外の値の 16 ビット符号なし整数です。 TNEF を使用しているサービス プロバイダーによって、 [OpenTnefStream](opentnefstream.md)関数に渡される最初の値から順番に各添付ファイルには、添付ファイルの参照キーが割り当てられます。 サービス プロバイダーは、2 つのメッセージが同じキーを使用する可能性を最小限に抑えるためのキーの場合は、ランダムな初期値を生成します。 
  
TNEF の実装では、対応する MAPI プロパティに属性をマップするのに属性の識別子を使用します。 属性識別子は、2 つの word 値の 32 ビットの符号なし整数です。 上位ワードのデータ型を示す文字列やバイナリなどと、下位ワードは、特定の属性を識別します。 上位 word 内のデータ型は次のとおりです。
  
|**型**|**値**|
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
   
TNEF では、各属性の下位ワードの値が定義されています。H ヘッダー ファイルです。
  

