---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3ca7f2b32dd04bf46f1d150ad0d30213045f27e5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575842"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを 1 つのフォルダーから別のフォルダーにコピーまたは移動します。
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpSrcInterface_
  
> [in]コピーまたは移動するメッセージを含むフォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpSrcFolder_
  
> [in]コピーまたは移動するメッセージを含むフォルダーへのポインター。
    
 _lpMsgList_
  
> [in]コピーまたは移動するメッセージを識別するエントリ識別子の配列へのポインター。 
    
 _lpDestInterface_
  
> [in]コピーまたは移動されたメッセージの移動先フォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpDestFolder_
  
> [in]コピーまたは移動されたメッセージの移動先フォルダーへのポインター。 このフォルダーは開いている必要があります。
    
 _ulUIParam_
  
> [in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。 _lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 _lpProgress パラメーター_ は _、ulFlags_ で MESSAGE_DIALOGフラグが設定されていない限り無視されます。
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。 _lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 _lpProgress パラメーター_ は _、ulFlags_ で MESSAGE_DIALOGフラグが設定されていない限り無視されます。
    
 _ulFlags_
  
> [in]コピーまたは移動操作の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MESSAGE_DIALOG 
  
> 進行状況インジケーターの表示を要求します。
    
MESSAGE_MOVE 
  
> メッセージはコピーの代わりに移動する必要があります。 このMESSAGE_MOVE設定されていない場合は、メッセージがコピーされます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> コピー操作または移動操作が成功しました。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。 
    
## <a name="remarks"></a>注釈

**IMAPISupport::CopyMessages** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 メッセージ ストア プロバイダーは [、IMAPIFolder::CopyMessages](imapifolder-copymessages.md)の実装で **IMAPISupport::CopyMessages** を呼び出して、1 つ以上のメッセージを 1 つのフォルダーから別のフォルダーにコピーまたは移動できます。 **IMAPISupport::CopyMessages** 呼び出しの一環として、メッセージ ストア プロバイダーは MAPI に進行状況インジケーターを表示する必要を指定できます。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

