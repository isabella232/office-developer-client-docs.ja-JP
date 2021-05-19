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
  
メッセージ サービスを現在のプロファイルに追加し、新しく追加されたサービス UID を返します。
  
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

 _lpszService_
  
> [in]追加するメッセージ サービスの名前へのポインター。 このメッセージ サービス名は、MapiSvc.inf ファイル **の [Services]** セクションに表示される必要があります。 
    
 _lpszDisplayName_
  
> [in]追加するメッセージ サービスの表示名へのポインター。 メッセージ サービスが MapiSvc.inf ファイルの PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを設定している場合 _、lpszDisplayName_ パラメーターは無視されます。
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]メッセージ サービスのインストール方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE
  
> lpszService パラメーターと lpszDisplayName パラメーターを LPWSTR にキャストし、Unicode 文字列として解釈する必要があります。
    
SERVICE_NO_RESTART_WARNING
  
> プロファイルに新しいメッセージ サービスを追加する場合、MAPI サブシステムは、さまざまな状況と条件に基づいて、多くの場合、このアクションでプロファイルの再起動が必要Outlook。 SERVICE_NO_RESTART_WARNING フラグが含まれていない場合に、SERVICE_UI_ALWAYS フラグと SERVICE_UI_ALLOWED フラグに基づいて UI が許可され、少なくとも 1 つのプロセスが現在のプロファイルにログオンしている場合、この関数は「これらの変更を有効にするために Outlook を再起動する必要があります」というメッセージを表示します。 フラグをSERVICE_NO_RESTART_WARNINGすると、その警告メッセージの表示が抑制されます。
    
SERVICE_UI_ALLOWED
  
> 必要に応じて、メッセージ サービス構成 UI を使用できます。
    
SERVICE_UI_ALWAYS
  
> メッセージ サービスは、構成プロパティ シートを表示します。
    
 _lpuidService_
  
> [out]追加されたメッセージ サービスの UID へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND
  
> メッセージ サービス名は MapiSvc.inf の **[Services]** セクションに含めではありません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin2::CreateMsgServiceEx** メソッドは、現在のプロファイルにメッセージ サービスを追加します。 **CreateMsgServiceEx は** 、メッセージ サービスのエントリ ポイント関数を呼び出して、サービス固有の構成タスクを実行します。 _ulFlags_ パラメーター SERVICE_UI_ALLOWEDフラグが設定されている場合、インストール中のメッセージ サービスにプロパティ シートを表示して、ユーザーが設定を構成できます。 
  
MapiSvc.inf ファイルには、メッセージ サービスを構成するプロバイダーの一覧と、それぞれのプロパティが含まれる。 **CreateMsgServiceEx** は、まずメッセージ サービスの新しいプロファイル セクションを作成し、そのサービスのすべての情報を MapiSvc.inf ファイルからプロファイルにコピーし、プロバイダーごとに新しいセクションを作成します。 
  
MapiSvc.inf からすべての情報がコピーされた後、メッセージ サービスのエントリ ポイント関数 **MSGSERVICEENTRY** が  _ulContext_ パラメーターに設定された MSG_SERVICE_CREATE 値で呼び出されます。 **CreateMsgServiceEx** メソッドの _ulFlags_ パラメーターで SERVICE_UI_ALLOWED フラグが設定されている場合、メッセージ サービスのエントリ ポイント関数が呼び出された場合 _、ulUIParam_ パラメーターと _ulFlags_ パラメーターの値も渡されます。 サービス プロバイダーは、ユーザーがメッセージ サービスを構成できるよう、構成プロパティ シートを表示する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

引数 **CreateMsgServiceEx** _lpuidService_ が NULL ではない場合、プロファイルに追加されたメッセージ サービスの **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティが、そのプロファイルがポイントする **GUID** に返されます。 
  
_lpuidService_ **パラメーターの PR_SERVICE_UID** プロパティの値を [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに渡して、サービスを構成します。 
  
> [!CAUTION]
> MAPI Microsoft Outlook 2010の実装では、MAPI サブシステムMAPI_UNICODEサポートされません。使用すると失敗します。 
  
> [!IMPORTANT]
> IMsgServiceAdmin2 インターフェイスは、IMsgServiceAdmin インターフェイスを実装するオブジェクトと同じオブジェクトによって公開され、Outlook の MAPI サブシステムの実装を 2003 年から使用Outlookされています。 その IID は次のように定義されます:> `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING は、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は、次の値を使用してコードに追加できます。>`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

