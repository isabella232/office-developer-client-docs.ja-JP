---
title: TNEF タグ付きメッセージテキスト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419920"
---
# <a name="tnef-tagged-message-text"></a>TNEF タグ付きメッセージテキスト

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タグ付きメッセージテキストは、親メッセージ内の添付ファイルの位置を解決するために TNEF によって使用されます。 これは、添付ファイルの位置に、メッセージテキストにプレースホルダーを追加することによって行われます。 このプレースホルダーまたは attachment タグには、添付ファイルとその位置の解決方法が TNEF にわかるような方法で添付ファイルが記述されています。 タグの書式は次のとおりです。
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 オブジェクトのタイトル** \<\> **とファイル名は、添付ファイル自体から取得される値を含む変数です。 ** \<\> ** これらの値を使用できない場合、タイトルは添付ファイルの種類に基づいて TNEF によって既定で指定されます。 
  
**keynum\>変数には、TNEF によって添付ファイルに割り当てられた添付ファイルキーのテキスト表現が含まれてい\<** ます。 キーの基本値が[OpenTnefStreamEx](opentnefstreamex.md)呼び出しに渡されます。 **OpenTnefStreamEx**のすべての呼び出しでは、基本値を0にすることはできません。 ゼロにしない限り、ランタイムライブラリが提供する乱数ジェネレーターから、システム時間に基づく擬似乱数を使用することをお勧めします。
  
** \<トランスポート名\> **の変数には、 [OpenTnefStreamEx](opentnefstreamex.md)呼び出しに渡されたストリーム名、または**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティの値が含まれています。
  
> [!NOTE]
> メッセージテキストタグの**PR_ATTACH_TRANSPORT_NAME**プロパティと** \<トランスポート名\> **の変数には、実装しているトランスポートプロバイダーの名前とは無関係なものがあります。 これらのアイテムは、トランスポートプロバイダーおよびメッセージングシステムの添付ファイルの名前を表します。 
  
メッセージテキストは、トランスポートプロバイダーが[ITnef:: OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出して、タグ付きメッセージテキストを要求したときにタグ付けされます。 タグ付きテキストストリームから読み取る場合、TNEF は、 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティで指定されたインデックスで、メッセージテキストに含まれていた単一の文字を適切なタグに置き換えます。 タグ付きテキストストリームに書き込む場合、TNEF は受信データのタグをチェックし、関連付けられた添付ファイルを見つけて、タグを1つのスペース文字に置き換えます。
  
タグ付きメッセージテキストを使用すると、メッセージングシステムによってメッセージテキストに加えられたほとんどの変更に関係なく、トランスポートプロバイダーが添付ファイルの位置を保持することができます。
  

