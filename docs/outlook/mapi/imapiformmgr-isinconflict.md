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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d8f28a6b0a1633b0060f02af7e38ef058527eb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800550"
---
# <a name="imapiformmgrisinconflict"></a>IMAPIFormMgr::IsInConflict

  
  
**適用されます**: Outlook 
  
フォームに独自のメッセージの競合を処理できるかどうかを決定します。 メッセージとは競合している場合は複数のユーザーによって同時に編集されましたが。 パブリック フォルダー内のメッセージに可能性があります。
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a>Parameters

 _ulMessageFlags_
  
> [in]フラグは、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティ、メッセージの現在の状態を示すメッセージのコピーのビットマップへのポインター。
    
 _ulMessageStatus_
  
> [in]メッセージの状態に関する追加情報を提供するメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティからコピーしたクライアント定義またはプロバイダー定義のフラグのビットマスクです。
    
 _szMessageClass_
  
> [in]メッセージのメッセージ クラスの名前を示す文字列です。
    
 _pFolderFocus_
  
> [in]メッセージを含むフォルダーへのポインター。 _PFolderFocus_パラメーターは、(たとえば、メッセージは、別のメッセージに埋め込まれている) 場合、このようなフォルダーが存在しない場合、NULL にすることができます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> フォームは、独自のメッセージの競合を処理しません。
    
S_FALSE 
  
> フォームは、独自のメッセージの競合を処理または対象の情報が渡されたメッセージは競合ではないです。
    
## <a name="remarks"></a>備考

フォーム ビューアーは、特定のフォームが独自のメッセージの競合を処理していないかどうかを検出する**IMAPIFormMgr::IsInConflict**メソッドを呼び出します。 **IsInConflict**では、競合のフラグが存在する_ulMessageFlags_および_ulMessageStatus_パラメーターにビットマスクがチェックされます。 競合のフラグが設定されている場合、 **IsInConflict**は、 _szMessageClass_パラメーターに渡されるメッセージ クラスを解決し、フォームは、独自の競合を処理しない場合は、S_OK を返します。 **IsInConflict**は、フォームは、独自の競合を処理する場合に S_FALSE を返します。 
  
独自の競合を処理しないフォームでは、 [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)メソッドを使用して開く必要があり、既存のフォーム オブジェクトを再利用することはできません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

クライアント アプリケーションは、通常、フォルダー内の次または前のメッセージを 1 つのメッセージから、アプリケーションが移動するときに、競合に対処するあります。 メッセージが競合しているがそのメッセージのフォームのサーバーの競合を処理できる場合は、クライアント アプリケーションは、次または前のメッセージを表示するため、通常のコードを実行する必要があります。 フォームのサーバーには、競合を処理できません、クライアント アプリケーションは必要がありますの次または前のメッセージのメッセージ クラスに気付いていなかったかのように進みます。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)
  
[PidTagMessageFlags の標準的なプロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus の標準的なプロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)

