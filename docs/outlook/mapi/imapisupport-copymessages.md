---
title: imapisupportcopymessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9cc4e3ba77395e09a6b95e8381fa402fc3cdff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405157"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを1つのフォルダーから別のフォルダーにコピーまたは移動します。
  
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

 _lpsrcinterface_
  
> 順番コピーまたは移動するメッセージを含むフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpsrcfolder_
  
> 順番コピーまたは移動するメッセージを含むフォルダーへのポインター。
    
 _lpmsglist_
  
> 順番コピーまたは移動するメッセージを識別するエントリ識別子の配列へのポインター。 
    
 _lpdestinterface_
  
> 順番コピーまたは移動されたメッセージの宛先フォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpdestfolder_
  
> 順番コピーまたは移動されたメッセージの宛先フォルダーへのポインター。 このフォルダーは開いている必要があります。
    
 _uluiparam_
  
> 順番進行状況インジケーターを表示する progress オブジェクトへのポインター。 _lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 MESSAGE_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。
    
 _lpprogress_
  
> 順番進行状況インジケーターを表示する progress オブジェクトへのポインター。 _lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 MESSAGE_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。
    
 _ulFlags_
  
> 順番コピー操作または移動操作の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MESSAGE_DIALOG 
  
> 進行状況インジケーターの表示を要求します。
    
MESSAGE_MOVE 
  
> メッセージはコピーではなく移動する必要があります。 MESSAGE_MOVE が設定されていない場合は、メッセージがコピーされます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> コピーまたは移動操作が正常に完了しました。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>注釈

**imapisupport:: copymessages**メソッドは、メッセージストアプロバイダーサポートオブジェクトに実装されています。 メッセージストアプロバイダーは、imapisupport [:: copymessages](imapifolder-copymessages.md)を使用して、1つまたは複数のメッセージを別のフォルダーにコピーまたは移動する**imapisupport:: copymessages**を呼び出すことができます。 **imapisupport:: copymessages**呼び出しの一部として、メッセージストアプロバイダーは MAPI が進行状況インジケーターを表示するように指定できます。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

