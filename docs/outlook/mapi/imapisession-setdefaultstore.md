---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e3c4125bf4fcf1881a0cba9b04a8bb6aa71f527d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800700"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**適用対象**: Outlook 
  
セッションの既定のメッセージ ストアとしてのメッセージ ・ ストアを確立します。
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]既定のメッセージ ストアの設定を制御するフラグのビットマスクです。 これらのフラグは相互に排他的です。次のフラグの 1 つだけを設定することができます。
    
MAPI_DEFAULT_STORE
  
> セッションのデフォルト値としては、メッセージ ・ ストアを確立します。 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) の列に STATUS_DEFAULT_STORE フラグを設定することによって、メッセージ ストアの状態のテーブルの行を更新します。
    
MAPI_PRIMARY_STORE
  
> ログオン時に使用するストアとしては、メッセージ ・ ストアを確立します。 メッセージ ストアは既定のストアではない場合、クライアントにたどれるように既定値です。 **PR_RESOURCE_FLAGS**列に STATUS_PRIMARY_STORE フラグを設定することによって、メッセージ ストアの状態のテーブルの行を更新します。 
    
MAPI_SECONDARY_STORE
  
> プライマリ メッセージ ストアを使用できない場合に、ログオンに使用するストアとしては、メッセージ ・ ストアを確立します。 クライアントは、プライマリ ストアを開くことができません、する場合はセカンダリ ・ ストアを開く必要があります、既定値として設定します。 **PR_RESOURCE_FLAGS**列に STATUS_SECONDARY_STORE フラグを設定することによって、メッセージ ストアの状態のテーブルの行を更新します。 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> その状態テーブルの行をメッセージ ストアのテーブルの行、およびセッション ・ プロファイル内のメッセージ ストアの**PR_RESOURCE_FLAGS**プロパティでは、STATUS_SIMPLE_STORE フラグを設定します。 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> 状態テーブルの行に、メッセージ ストアのテーブルの行に、メッセージ ストアの**PR_RESOURCE_FLAGS**プロパティに STATUS_SIMPLE_STORE フラグを設定します。 プロファイルは変更されません。 
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]既定では、メッセージ ・ ストアのエントリの識別子へのポインター。 場合は_lpEntryID_に NULL を渡すと、クライアント、メッセージ ・ ストアが選択されていない既定値としてします。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>注釈

**IMAPISession::SetDefaultStore**メソッドは、次のいずれかとしてメッセージ ストアを確立します。 
  
- セッションの既定のメッセージ ストアです。
    
- セッションの主なメッセージ ・ ストアです。
    
- セッションの第 2 のメッセージ ・ ストアです。
    
メッセージ ストアを確立すると、既定値として、メッセージ ・ ストアは、次のフラグで、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティを設定する必要があります。
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>呼び出し側への注意

状態テーブルを取得して、 **PR_RESOURCE_FLAGS**の列に STATUS_DEFAULT_STORE フラグの設定を検索して、セッションの既定のメッセージ ストアを指定できます。 この設定を持つ行は、セッションのデフォルト値として指定されているメッセージ ・ ストアを表します。 
  
MAPI_DEFAULT_STORE または MAPI_SIMPLE_STORE_PERMANENT フラグを設定すると、MAPI は、プロファイル、メッセージ ストアのテーブル、およびテーブルのステータスを更新します。 
  
メッセージ ストアの既定の設定を変更、ときに、次の通知が生成されます。
  
- **FnevTableModified**イベント通知は、メッセージ ストアとステータスの表には影響を受ける行ごとに発行されます。 
    
- 内部の通知は、MAPI スプーラーに発行されます。 既に進行中の操作が完了した変更です。新しい既定のストアの既定のメッセージ ストアのメッセージをダウンロードするなど、新しい操作が処理されます。
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |MFCMAPI では、 **IMAPISession::SetDefaultStore**メソッドを使用して、既定のストアとして選択されているストアを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[PidTagResourceFlags 標準プロパティ](pidtagresourceflags-canonical-property.md)
  
[PidTagStoreSupportMask 標準プロパティ](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

