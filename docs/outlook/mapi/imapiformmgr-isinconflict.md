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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321848"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームが独自のメッセージ競合を処理できるかどうかを決定します。 メッセージが複数のユーザーによって同時に編集されている場合、メッセージは競合しています。 これは、パブリックフォルダー内のメッセージに発生する可能性があります。
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>パラメーター

 _ulmessageflags_
  
> 順番メッセージの現在の状態を示す、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。
    
 _ulmessagestatus_
  
> 順番メッセージの状態に関する追加情報を提供する、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされた、クライアント定義またはプロバイダー定義のフラグのビットマスク。
    
 _szmessageclass_
  
> 順番メッセージのメッセージクラスの名前を表す文字列。
    
 _pfolderfocus_
  
> 順番メッセージを含むフォルダーへのポインター。 このようなフォルダーが存在しない場合 (たとえば、メッセージが別のメッセージに埋め込まれている場合) は、 _pfolderfocus_パラメーターを NULL にすることができます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームでは、独自のメッセージの競合は処理されません。
    
S_FALSE 
  
> フォームが独自のメッセージ競合を処理するか、渡された情報が競合していないことを示すメッセージを表示します。
    
## <a name="remarks"></a>解説

フォームビューアーは、 **imapiformmgr:: IsInConflict**メソッドを呼び出して、特定のフォームが独自のメッセージ競合を処理していないかどうかを検出します。 **IsInConflict**は、競合フラグが存在するかどうかについて、 _ulmessageflags_および_ulmessageflags_パラメーターのビットマスクをチェックします。 競合フラグが設定されている場合、 **IsInConflict**は、 _szmessageclass_パラメーターで渡されたメッセージクラスを解決し、フォームが自身の競合を処理していない場合は S_OK を返します。 フォームが自身の競合を処理する場合、 **IsInConflict**は S_FALSE を返します。 
  
独自の競合を処理しないフォームは、 [imapiformmgr:: loadform](imapiformmgr-loadform.md)メソッドを使用して開く必要があります。また、既存の form オブジェクトを再利用することはできません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

通常、クライアントアプリケーションは、あるメッセージからフォルダー内の次または前のメッセージにアプリケーションが移動したときに、競合を処理する必要があります。 メッセージが競合していても、そのメッセージのフォームサーバーが競合を処理できる場合、クライアントアプリケーションは、次のメッセージまたは前のメッセージを表示するために、通常のコードを実行する必要があります。 フォームサーバーが競合を処理できない場合は、次または前のメッセージのメッセージクラスを認識していない場合と同様に、クライアントアプリケーションを続行する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

