---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b14c4476ab4fd1e9891331da0792fc9846702659
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556561"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッションの既定のメッセージ ストアとしてメッセージ ストアを確立します。
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]既定のメッセージ ストアの設定を制御するフラグのビットマスク。 これらのフラグは相互に排他的です。設定できるフラグは次の 1 つのみです。
    
MAPI_DEFAULT_STORE
  
> セッションの既定値としてメッセージ ストアを確立します。 メッセージ ストアの状態テーブル行を更新するには、STATUS_DEFAULT_STORE **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 列の PR_RESOURCE_FLAGS フラグを設定します。
    
MAPI_PRIMARY_STORE
  
> ログオン時に使用するストアとしてメッセージ ストアを確立します。 メッセージ ストアが既定のストアではない場合、クライアントは既定のストアにする必要があります。 メッセージ ストアの状態テーブルの行を更新するには、STATUS_PRIMARY_STORE列の [PR_RESOURCE_FLAGS] **フラグをPR_RESOURCE_FLAGS** します。 
    
MAPI_SECONDARY_STORE
  
> プライマリ メッセージ ストアが使用できない場合、ログオン時に使用するストアとしてメッセージ ストアを確立します。 クライアントがプライマリ ストアを開けできない場合は、セカンダリ ストアを開き、既定として設定する必要があります。 メッセージ ストアの状態テーブルの行を更新するには、STATUS_SECONDARY_STORE列の [PR_RESOURCE_FLAGS] **フラグをPR_RESOURCE_FLAGS** します。 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> メッセージ ストアの STATUS_SIMPLE_STORE プロパティの状態テーブル行、メッセージ ストア **テーブル行、および** セッション プロファイルの PR_RESOURCE_FLAGS フラグを設定します。 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> メッセージ ストアのSTATUS_SIMPLE_STOREのステータス テーブル行とメッセージ ストア **テーブル行** PR_RESOURCE_FLAGSプロパティのプロパティのフラグを設定します。 プロファイルは変更されません。 
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]既定のメッセージ ストアのエントリ識別子へのポインター。 クライアントが  _lpEntryID_ で NULL を渡した場合、既定ではメッセージ ストアは選択されません。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
## <a name="remarks"></a>注釈

**IMAPISession::SetDefaultStore** メソッドは、次のいずれかのメッセージ ストアを確立します。 
  
- セッションの既定のメッセージ ストア。
    
- セッションのプライマリ メッセージ ストア。
    
- セッションのセカンダリ メッセージ ストア。
    
メッセージ ストアを既定として確立するには、メッセージ ストアのポリシー [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)プロパティに次のフラグ **PR_STORE_SUPPORT_MASK** 設定されている必要があります。
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>呼び出し側への注意

セッションの既定のメッセージ ストアを確認するには、状態テーブルを取得し、STATUS_DEFAULT_STORE 列の STATUS_DEFAULT_STORE フラグ **の設定をPR_RESOURCE_FLAGS** します。 この設定を持つ行は、セッションの既定値として指定されているメッセージ ストアを表します。 
  
[メッセージ ストア] MAPI_DEFAULT_STOREまたは MAPI_SIMPLE_STORE_PERMANENTフラグが設定されている場合、MAPI はプロファイル、メッセージ ストア テーブル、および状態テーブルを更新します。 
  
メッセージ ストアの既定の設定に変更が加わるたびに、次の通知が生成されます。
  
- **メッセージ ストアと状態テーブルの両方** の影響を受ける行ごとに、fnevTableModified イベント通知が発行されます。 
    
- 内部通知が MAPI スプーラーに発行されます。 既に進行中の操作は変更なしで完了します。メッセージのダウンロードなど、既定のメッセージ ストアを含む新しい操作が、新しい既定のストアに対して処理されます。
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |MFCMAPI は **IMAPISession::SetDefaultStore** メソッドを使用して、選択したストアを既定のストアとして設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[PidTagResourceFlags 標準プロパティ](pidtagresourceflags-canonical-property.md)
  
[PidTagStoreSupportMask 標準プロパティ](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

