---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412885"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームが独自のメッセージ競合を処理できるかどうかを決定します。 複数のユーザーが同時に編集した場合、メッセージが競合しています。 これは、パブリック フォルダー内のメッセージに発生する可能性があります。
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>パラメーター

 _ulMessageFlags_
  
> [in]メッセージの現在の状態を示すメッセージの **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。
    
 _ulMessageStatus_
  
> [in]メッセージの状態に関する追加情報を提供するメッセージの **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされたクライアント定義フラグまたはプロバイダー定義フラグのビットマスク。
    
 _szMessageClass_
  
> [in]メッセージのメッセージ クラスの名前を指定する文字列。
    
 _pFolderFocus_
  
> [in]メッセージを含むフォルダーへのポインター。 _pFolderFocus_ パラメーターは、そのようなフォルダーが存在しない場合は NULL にできます (たとえば、メッセージが別のメッセージに埋め込まれている場合)。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームは、独自のメッセージ競合を処理しない。
    
S_FALSE 
  
> フォームは、独自のメッセージ競合を処理するか、渡された情報のメッセージが競合していない。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormMgr::IsInConflict** メソッドを呼び出して、特定のフォームが独自のメッセージ競合を処理していないかどうかを検出します。 **IsInConflict は**_、ulMessageFlags_ パラメーターと _ulMessageStatus_ パラメーターのビットマスクをチェックして、競合フラグの有無を確認します。 競合フラグが設定されている場合 **、IsInConflict** は  _szMessageClass_ パラメーターで渡されたメッセージ クラスを解決し、フォームが独自の競合を処理しない場合は S_OK を返します。 **IsInConflict は** 、フォームS_FALSE競合を処理する場合に、この値を返します。 
  
独自の競合を処理しないフォームは [、IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) メソッドを使用して開く必要があります。既存のフォーム オブジェクトを再利用することはできません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

通常、クライアント アプリケーションは、アプリケーションがフォルダー内の 1 つのメッセージから次のメッセージまたは前のメッセージに移動するときに競合に対処する必要があります。 メッセージが競合しているが、そのメッセージのフォーム サーバーが競合を処理できる場合、クライアント アプリケーションは、次または前のメッセージを表示するための通常のコードを実行する必要があります。 フォーム サーバーが競合を処理できない場合、クライアント アプリケーションは、次または前のメッセージのメッセージ クラスを知らなかった場合と同様に続行する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

