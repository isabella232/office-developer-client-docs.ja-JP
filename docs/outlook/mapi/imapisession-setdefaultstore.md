---
title: imapisessionsetdefaultstore
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
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335806"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッションの既定のメッセージストアとしてメッセージストアを確立します。
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番既定のメッセージストアの設定を制御するフラグのビットマスク。 これらのフラグは相互に排他的です。設定できるのは、次に示すフラグのいずれか1つだけです。
    
MAPI_DEFAULT_STORE
  
> セッションの既定値としてメッセージストアを確立します。 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 列の STATUS_DEFAULT_STORE フラグを設定して、メッセージストアの状態テーブルの行を更新します。
    
MAPI_PRIMARY_STORE
  
> ログオン時に使用するストアとして、メッセージストアを確立します。 メッセージストアが既定のストアではない場合、クライアントは既定のストアにする必要があります。 **PR_RESOURCE_FLAGS**列の STATUS_PRIMARY_STORE フラグを設定して、メッセージストアの状態テーブルの行を更新します。 
    
MAPI_SECONDARY_STORE
  
> プライマリメッセージストアが使用できない場合に、ログオン時に使用するストアとしてメッセージストアを確立します。 クライアントがプライマリストアを開くことができない場合は、セカンダリストアを開き、既定として設定する必要があります。 **PR_RESOURCE_FLAGS**列の STATUS_SECONDARY_STORE フラグを設定して、メッセージストアの状態テーブルの行を更新します。 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> [状態] テーブル行、メッセージストアテーブル行、およびセッションプロファイルで、メッセージストアの**PR_RESOURCE_FLAGS**プロパティの STATUS_SIMPLE_STORE フラグを設定します。 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> STATUS_SIMPLE_STORE フラグを、状態テーブルの行とメッセージストアの表の行の**PR_RESOURCE_FLAGS**プロパティに設定します。 プロファイルは変更されません。 
    
 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番既定として使用するメッセージストアのエントリ識別子へのポインター。 クライアントが_lな tryid_で NULL を渡す場合、既定としてメッセージストアが選択されていません。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
## <a name="remarks"></a>解説

**imapisession:: setdefaultstore**メソッドは、次のいずれかのようにメッセージストアを確立します。 
  
- セッションの既定のメッセージストア。
    
- セッションのプライマリメッセージストア。
    
- セッションのセカンダリメッセージストア。
    
メッセージストアを既定として設定するには、メッセージストアの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティに次のフラグが設定されている必要があります。
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>呼び出し側への注意

[状態] テーブルを取得し、 **PR_RESOURCE_FLAGS**列の STATUS_DEFAULT_STORE フラグの設定を検索することによって、セッションの既定のメッセージストアを判別できます。 この設定の行は、セッションの既定値として指定されたメッセージストアを表します。 
  
MAPI_DEFAULT_STORE または MAPI_SIMPLE_STORE_PERMANENT フラグが設定されている場合は、MAPI がプロファイル、メッセージストアテーブル、および状態テーブルを更新します。 
  
メッセージストアの既定の設定が変更されるたびに、次の通知が生成されます。
  
- **fnevTableModified**イベント通知は、メッセージストアと状態テーブルの両方の影響を受ける各行に対して発行されます。 
    
- MAPI スプーラーに内部通知が発行されます。 進行中の操作は、変更されずに完了します。既定のメッセージストア (メッセージのダウンロードなど) に関連する新しい操作は、新しい既定のストアに対して処理されます。
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|maindlg .cpp  <br/> |CMainDlg:: OnSetDefaultStore  <br/> |mfcmapi は、 **imapisession:: setdefaultstore**メソッドを使用して、選択されたストアを既定のストアとして設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[PidTagResourceFlags 標準プロパティ](pidtagresourceflags-canonical-property.md)
  
[PidTagStoreSupportMask 標準プロパティ](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

