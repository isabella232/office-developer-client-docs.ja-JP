---
title: メッセージを読むフォームを起動する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d12801658fde2155367090f48d23ca969f39b8fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561314"
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

