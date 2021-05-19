---
title: メッセージを読むフォームを起動する
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
# <a name="launching-a-form-to-read-a-message"></a>メッセージを読むフォームを起動する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム サーバーの実装者は、クライアント アプリケーションがメッセージを読み込むときに、フォーム サーバーとフォーム オブジェクトへのメソッド呼び出しの次のシーケンスを期待する必要があります。
  
1. クライアント アプリケーションは [、MAPIOpenFormMgr](mapiopenformmgr.md) 関数を呼び出してフォーム マネージャーを開きます。 
    
2. クライアント アプリケーションは [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) メソッドを呼び出し [、IMAPIForm](imapiformiunknown.md)を持つオブジェクトを返します。 フォーム マネージャーがフォームのアクティブ化に使用されない場合は、フォーム マネージャーがリリースされる可能性があります。 LoadForm の呼び出し **には** 、フォーム マネージャーがフォーム サーバーの実行可能ファイルをインストールしてから進む必要がある場合があります。 
    
3. 必要に応じて、クライアント アプリケーションは [IMAPIViewContext](imapiviewcontextiunknown.md) を準備して、フォーム オブジェクトがフォルダー内の前または次のメッセージを読み込む可能性がある操作を制御できます。 クライアント アプリケーションでは [、IMAPIForm::SetViewContext](imapiform-setviewcontext.md) メソッドを使用して **、LoadForm** 呼び出しで設定された既定のビュー コンテキストを変更できます。 
    
4. クライアント アプリケーションは [、IPersistMessage::Load](ipersistmessage-load.md) メソッドを呼び出して、メッセージ データをフォーム オブジェクトに読み込む。 
    
5. クライアント アプリケーションは [IMAPIForm::D oVerb](imapiform-doverb.md) を呼び出して、開いている動詞を呼び出し、オプションの [IMAPIViewContext](imapiviewcontextiunknown.md) インターフェイス ポインターを渡します。 
    
## <a name="see-also"></a>関連項目



[フォーム サーバーの操作](form-server-interactions.md)

