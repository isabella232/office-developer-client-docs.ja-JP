---
title: メッセージを読むためのフォームの起動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b9166090321aa24e35fe1c82908aec0c403095cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593740"
---
# <a name="launching-a-form-to-read-a-message"></a>メッセージを読むためのフォームの起動

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム サーバーの実装では、クライアント アプリケーションがメッセージを読み込むとき、サーバーのフォームとフォーム オブジェクトのメソッド呼び出しの次の順序の期待される結果必要があります。
  
1. クライアント アプリケーションは、 [MAPIOpenFormMgr](mapiopenformmgr.md)関数を呼び出して、フォーム マネージャーを開きます。 
    
2. クライアント メソッドを呼び出して、 [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) 、 [IMAPIForm](imapiformiunknown.md)を使用してオブジェクトを返します。 さらにフォームのアクティブ化を使用しない場合、フォーム マネージャーを解放可能性があります。 フォーム マネージャーは、続行する前に、フォームのサーバーの実行可能ファイルをインストールする必要がありますので**LoadForm**への呼び出しは時間がかかることに注意してください。 
    
3. 必要に応じて、クライアント アプリケーションでは、フォルダー内の前または次のメッセージをロードするフォーム オブジェクトを引き起こす可能性のあるコントロールの操作に[IMAPIViewContext](imapiviewcontextiunknown.md)を準備できます。 クライアント アプリケーションは、 [IMAPIForm::SetViewContext](imapiform-setviewcontext.md)メソッドを使用して、設定された既定のビュー コンテキストを変更するのには**LoadForm**の呼び出しで。 
    
4. クライアント アプリケーションでは、form オブジェクトにメッセージのデータをロードするのには[IPersistMessage::Load](ipersistmessage-load.md)メソッドを呼び出します。 
    
5. クライアント アプリケーションでは、省略可能な[IMAPIViewContext](imapiviewcontextiunknown.md)インターフェイス ポインターを渡すこと、開いている動詞を呼び出すには、 [IMAPIForm::DoVerb](imapiform-doverb.md)を呼び出します。 
    
## <a name="see-also"></a>関連項目



[フォーム サーバーの相互作用](form-server-interactions.md)

