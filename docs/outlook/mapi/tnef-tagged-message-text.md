---
title: TNEF-Taggedメッセージ テキスト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d74b1c232cefe0233f97c196a968e2feed2d3b5a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624035"
---
# <a name="tnef-tagged-message-text"></a>TNEF-Taggedメッセージ テキスト

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タグ付きメッセージ テキストは、親メッセージ内の添付ファイルの位置を解決するために TNEF によって使用されます。 これは、添付ファイルの位置にメッセージ テキストに場所の所有者を追加することで行われます。 この場所の所有者 (添付ファイル タグ) は、TNEF が添付ファイルとその位置を解決する方法を知っている方法で添付ファイルを記述します。 タグの形式は次のとおりです。
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 **\<Object Title\>** 添付 **\<File Name\>** ファイル自体から取り出される値を含む変数です。 これらの値を使用できない場合、タイトルの既定値は添付ファイルの種類に基づいて TNEF です。 
  
変数には、TNEF によって添付ファイルに割り当てられた添付ファイル **\<KeyNum\>** キーのテキスト表現が含まれる。 キーの基本値は [、OpenTnefStreamEx 呼び出しに渡](opentnefstreamex.md) されます。 基本値を 0 にし **、OpenTnefStreamEx** の呼び出しごとに同じ値にしない必要があります。 実行時ライブラリが提供する任意の乱数ジェネレーターからのシステム時間に基づいて擬似乱数を使用すれば十分です。これらの乱数がゼロではないと保証されている限りです。
  
変数 **\<Transport Name\>** には [、OpenTnefStreamEx](opentnefstreamex.md) 呼び出しに渡されるストリーム名、または **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティの値が含まれます。
  
> [!NOTE]
> メッセージ **PR_ATTACH_TRANSPORT_NAME** タグ内の PR_ATTACH_TRANSPORT_NAME プロパティと変数は、実装するトランスポート プロバイダーの名前とは **\<Transport Name\>** 関係しません。 これらのアイテムは、トランスポート プロバイダーとメッセージング システムの添付ファイルの名前を表します。 
  
メッセージ テキストは、トランスポート プロバイダーが [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) メソッドを呼び出してタグ付けされたメッセージ テキストを求めるときにタグ付けされます。 タグ付きテキスト ストリームから読み取る場合 **、TNEF は、PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティで指定されたインデックスにあるメッセージ テキスト内の 1 文字を適切なタグに置き換える。 タグ付きテキスト ストリームに書き込む場合、TNEF はタグの受信データをチェックし、関連付けられた添付ファイルを検索し、タグを 1 つのスペース文字に置き換える。
  
タグ付きメッセージ テキストを使用すると、メッセージング システムによってメッセージ テキストに加えたほとんどの変更に関係なく、トランスポート プロバイダーは添付ファイルの位置を保持できます。
  

