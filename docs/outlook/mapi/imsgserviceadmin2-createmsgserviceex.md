---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410183"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のプロファイルにメッセージサービスを追加し、新しく追加されたサービス UID を返します。
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a>パラメーター

 _lpszservice_
  
> 順番追加するメッセージサービスの名前へのポインター。 このメッセージサービス名は、mapisvc.inf ファイルの **[Services]** セクションに表示される必要があります。 
    
 _lpszdisplayname_
  
> 順番追加するメッセージサービスの表示名へのポインター。 メッセージサービスが mapisvc.inf ファイルで**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを設定している場合、 _lpszdisplayname_パラメーターは無視されます。
    
 _uluiparam_
  
> 順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> 順番メッセージサービスのインストール方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE
  
> lpszservice および lpszservice パラメーターは、LPWSTR にキャストし、Unicode 文字列として解釈される必要があります。
    
SERVICE_NO_RESTART_WARNING
  
> プロファイルに新しいメッセージサービスを追加すると、さまざまな状況や条件に基づいて MAPI サブシステムが、Outlook の再起動が必要であると判断されることがよくあります。 SERVICE_NO_RESTART_WARNING フラグが含まれておらず、SERVICE_UI_ALWAYS と SERVICE_UI_ALLOWED フラグに基づいて UI が許可されていて、少なくとも1つのプロセスが現在のプロファイルに記録されている場合、この関数は "Outlook を再起動する必要があります。" というメッセージを表示します。これらの変更は有効になります。 SERVICE_NO_RESTART_WARNING フラグを含めると、その警告メッセージの表示が抑制されます。
    
SERVICE_UI_ALLOWED
  
> 必要に応じて、メッセージサービス構成 UI を使用できます。
    
SERVICE_UI_ALWAYS
  
> メッセージサービスには、その構成プロパティシートが表示されます。
    
 _lpuidservice_
  
> 読み上げ追加されたメッセージサービスの UID へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND
  
> メッセージサービス名が mapisvc.inf の **[Services]** セクションにありません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin2:: CreateMsgServiceEx**メソッドは、現在のプロファイルにメッセージサービスを追加します。 **CreateMsgServiceEx**は、メッセージサービスのエントリポイント関数を呼び出して、サービス固有の構成タスクを実行します。 SERVICE_UI_ALLOWED フラグが_ulflags_パラメーターで設定されている場合は、インストールされているメッセージサービスでプロパティシートを表示して、ユーザーが設定を構成できるようにすることができます。 
  
mapisvc.inf ファイルには、メッセージサービスを構成するプロバイダーの一覧とそれぞれのプロパティが含まれています。 **CreateMsgServiceEx**は、最初にメッセージサービス用の新しいプロファイルセクションを作成し、そのサービスのすべての情報を mapisvc.inf ファイルからプロファイルにコピーして、各プロバイダーに新しいセクションを作成します。 
  
すべての情報が mapisvc.inf からコピーされた後、メッセージサービスのエントリポイント関数である**msgserviceentry**が、 _ulcontext_パラメーターで設定された MSG_SERVICE_CREATE 値を使用して呼び出されます。 SERVICE_UI_ALLOWED フラグが**CreateMsgServiceEx**メソッドの_ulflags_パラメーターで設定されている場合は、メッセージサービスのエントリポイント関数が呼び出されたときに、 _uluiparam_パラメーターと_ulflags_パラメーターの値も渡されます。 サービスプロバイダーは、ユーザーがメッセージサービスを構成できるように、その構成プロパティシートを表示する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CreateMsgServiceEx** _lpuidservice_引数が NULL でない場合、プロファイルに追加されたメッセージサービスの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティが、ポイントした**GUID**で返されます。 
  
_lpuidservice_パラメーターの**PR_SERVICE_UID**プロパティの値を[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに渡して、サービスを構成します。 
  
> [!CAUTION]
> MAPI サブシステムの Microsoft Outlook 2010 実装は MAPI_UNICODE をサポートしていないため、使用されている場合は失敗します。 
  
> [!IMPORTANT]
> IMsgServiceAdmin2 インターフェイスは、IMsgServiceAdmin インターフェイスを実装するのと同じオブジェクトで公開されており、outlook 2003 以降の outlook の MAPI サブシステムの実装を使用して利用できるようになっています。 その IID は、次のように`#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`定義されています。 > > 現在のダウンロード可能なヘッダーファイルで_ulflags_ SERVICE_NO_RESTART_WARNING が定義されていない場合があります。その場合は、次の値を使用してコードに追加できます。 >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

