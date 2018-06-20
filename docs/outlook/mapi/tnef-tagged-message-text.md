---
title: メッセージの TNEF のタグ付きテキスト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bedfc0457b0de8287a4e7bc8bdf8fb57404e4fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804116"
---
# <a name="tnef-tagged-message-text"></a>メッセージの TNEF のタグ付きテキスト

  
  
**適用されます**: Outlook 
  
タグ付きのメッセージのテキストは、親メッセージの添付ファイルの位置を解決するのには TNEF が使用されます。 これは、は、添付ファイルの位置にあるメッセージのテキストのプレース ホルダーを追加することによって行われます。 このプレース ホルダー、または添付ファイルのタグは、TNEF 添付ファイルとの位置を解決する方法を知っていることのような方法で添付ファイルを説明します。 タグの形式は次のとおりです。
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 **\<オブジェクトのタイトル\>** と**\<ファイル名\>** は、添付ファイル自体から取得される値を含む変数です。 これらの値は利用できませんの場合、タイトルは TNEF の添付ファイルの種類に基づいて、デフォルトとして使用します。 
  
** \<KeyNum\>** 変数には、TNEF 添付ファイルに割り当てられている添付ファイルのキーのテキスト表現が含まれています。 基本キーの値が渡される[OpenTnefStreamEx](opentnefstreamex.md)の呼び出しにします。 基本値は 0 にできませんする必要があり、 **OpenTnefStreamEx**を呼び出すたびに同じにしないで。 システム時間に基づいて、実行時ライブラリが用意されています、どのようなランダム番号ジェネレーターから 0 であることを保証する限り、擬似乱数を使用することで十分です。
  
**\<トランスポート名\>** [OpenTnefStreamEx](opentnefstreamex.md)の呼び出しまたは**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティの値に渡されるストリーム名が変数に含まれています。
  
> [!NOTE]
> **PR_ATTACH_TRANSPORT_NAME**プロパティと**\<トランスポート名\>** を実装するトランスポート プロバイダーの名前とは何もメッセージのテキストのタグ内の変数があります。 これらのアイテムは、トランスポート プロバイダーが、メッセージング システムの添付ファイルの名前を表します。 
  
トランスポート プロバイダーは、 [ITnef::OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出すことによってタグ付けされたメッセージ テキストのメッセージが表示されたら、メッセージのテキストがタグ付けされます。 タグ付きテキスト ストリームから読み取る場合、TNEF は、適切なタグを使用して**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) のプロパティに指定したメッセージ テキストの 1 つの文字を置き換えます。 タグ付きのテキスト ストリームに書き込む場合、TNEF タグの受信データを確認、関連付けられている添付ファイルを検索、タグを 1 つの空白文字に置き換えます。
  
タグ付けされたメッセージのテキストを使用すると、トランスポート プロバイダーを維持できる、メッセージング システムがメッセージのテキストに加えた変更のほとんどに関係なく、添付ファイルの位置に注意してください。
  

