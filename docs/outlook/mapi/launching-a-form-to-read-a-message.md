---
title: メッセージを読むためのフォームの起動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 439927dc78941f086c025d77c76236497d3f4a15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425933"
---
# <a name="launching-a-form-to-read-a-message"></a>メッセージを読むためのフォームの起動

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームサーバーの実装者は、クライアントアプリケーションがメッセージを読み込むときに、次のようなフォームサーバーとフォームオブジェクトのメソッド呼び出しを想定してください。
  
1. クライアントアプリケーションは、 [MAPIOpenFormMgr](mapiopenformmgr.md)関数への呼び出しを使用してフォームマネージャーを開きます。 
    
2. クライアントアプリケーションは、 [imapiformmgr:: loadform](imapiformmgr-loadform.md)メソッドを呼び出します。このメソッドは[imapiform](imapiformiunknown.md)を使用してオブジェクトを返します。 フォームマネージャーがさらにフォームのアクティブ化に使用されない場合は、今リリースされる可能性があります。 作業を進める前に、フォームマネージャーがフォームサーバーの実行可能ファイルをインストールする必要がある場合があるため、 **loadform**の呼び出しには時間がかかる場合があります。 
    
3. 必要に応じて、クライアントアプリケーションで[imapiviewcontext](imapiviewcontextiunknown.md)を準備し、form オブジェクトがフォルダー内の前または次のメッセージを読み込むことができる操作を制御することができます。 クライアントアプリケーションは、 [imapiform:: setviewcontext](imapiform-setviewcontext.md)メソッドを使用して、 **loadform**呼び出しで設定された既定のビューコンテキストを変更できます。 
    
4. クライアントアプリケーションは、 [IPersistMessage:: Load](ipersistmessage-load.md)メソッドを呼び出して、メッセージデータを form オブジェクトに読み込みます。 
    
5. クライアントアプリケーションは、 [imapiform を呼び出します。:D overb](imapiform-doverb.md)を呼び出して open 動詞を呼び出し、省略可能な[imapiform](imapiviewcontextiunknown.md)インターフェイスポインターを渡します。 
    
## <a name="see-also"></a>関連項目



[フォームサーバーの相互作用](form-server-interactions.md)

