---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bac363183c15a2d53c15b46724266b6cb5744075
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800490"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**適用対象**: Outlook 
  
(たとえば、あるかどうかそのメッセージは削除対象としてマーク) は、特定のフォルダー内のメッセージに関連付けられたステータスを取得します。
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]状態が取得したメッセージのエントリの識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulMessageStatus_
  
> [out]メッセージのステータスを示すフラグのビットマスクへのポインターへのポインター。 ビット 0 ~ 15 は予約されており、0 にする必要があります。31 までの 16 ビットは、実装固有の用途に使用できます。 次のフラグを設定することができます。
    
MSGSTATUS_DELMARKED 
  
> メッセージは、削除対象としてマークされています。
    
MSGSTATUS_HIDDEN 
  
> メッセージは表示しません。 
    
MSGSTATUS_HIGHLIGHTED 
  
> メッセージが表示されるが強調表示されています。
    
MSGSTATUS_REMOTE_DELETE 
  
> メッセージは、ローカル クライアントにダウンロードすることがなくリモート メッセージ ストアを削除対象としてマークされています。
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> メッセージは、リモート メッセージ ストアからローカル クライアントにダウンロード用にマークされています。
    
MSGSTATUS_TAGGED 
  
> クライアント定義の目的は、メッセージをタグ付けされました。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージの状態が正常に取得しました。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::GetMessageStatus**メソッドは、メッセージのステータスを返します。 メッセージの状態は、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティに格納されます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

メッセージのステータス ビットを設定、オフになっていると使用する方法によって異なります完全に、実装がビット 0 ~ 15 は予約されており、0 にする必要があります。 IPM サブツリー内のメッセージを格納する場合、MAPI は IPM クライアントによってビット 16 ~ 31 の使用を予約します。 他のサブツリー内のメッセージを格納する場合は、目的に合わせて 31 までからの 16 ビットを使用できます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetNextMessage  <br/> |MFCMAPI では、 **IMAPIFolder::GetMessageStatus**メソッドを使用して、表示される次のメッセージのステータスを取得します。  <br/> |
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal と OpenMessageModal  <br/> |MFCMAPI では、 **IMAPIFolder::GetMessageStatus**メソッドを使用して、フォームのビューアーでは、CMyMAPIFormViewer または[IMAPISession::ShowForm](imapisession-showform.md)に渡すことを表示するメッセージのステータスを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

