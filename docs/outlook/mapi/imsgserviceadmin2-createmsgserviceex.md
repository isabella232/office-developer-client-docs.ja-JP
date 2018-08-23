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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3aae61f7b21c507da7955dbb4393d13bfb5fa24c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800981"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**適用対象**: Outlook 
  
サービス UID を新しく追加すること、現在のプロファイルには、メッセージ サービスを追加します。
  
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
  
> [in]追加するのにはメッセージ サービスの名前へのポインター。 MapiSvc.inf ファイルの **[サービス]** セクションで、このメッセージのサービス名があります。 
    
 _lpszDisplayName_
  
> [in]追加するのにはメッセージ サービスの表示名へのポインター。 メッセージ サービスが、MapiSvc.inf ファイルの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを設定されている場合、 _lpszDisplayName_パラメーターは無視されます。
    
 _ulUIParam_
  
> [in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。
    
 _ulFlags_
  
> [in]メッセージ サービスをインストールする方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE
  
> LpszService および lpszDisplayName パラメーターを LPWSTR にキャストし、Unicode 文字列として解釈する必要があります。
    
SERVICE_NO_RESTART_WARNING
  
> 新しいメッセージ サービスをプロファイルに追加するときに多くの場合さまざまな状況や条件に基づき、MAPI サブシステムがアクションには、Outlook の再起動が必要ですを決定します。 SERVICE_NO_RESTART_WARNING フラグが含まれていない UI を使用すると-- SERVICE_UI_ALWAYS と SERVICE_UI_ALLOWED のフラグに基づくし、少なくとも 1 つのプロセスは、現在のプロファイルにログオンしている、この関数、メッセージが表示"する必要があります Outlook を再起動これらの変更を有効にする。」 SERVICE_NO_RESTART_WARNING フラグを含む、警告メッセージの表示を抑制します。
    
SERVICE_UI_ALLOWED
  
> メッセージ サービスの構成が必要な場合、UI は許可されています。
    
SERVICE_UI_ALWAYS
  
> メッセージ サービスでは、[設定] プロパティ シートが表示されます。
    
 _lpuidService_
  
> [out]追加メッセージ サービスの UID へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND
  
> メッセージ サービス名は、MapiSvc.inf の **[サービス]** セクションではありません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin2::CreateMsgServiceEx**メソッドは、メッセージ サービスを現在のプロファイルに追加します。 **CreateMsgServiceEx**は、サービス固有の構成タスクを実行するのには、メッセージ サービスのエントリ ポイント関数を呼び出します。 _UlFlags_パラメーターに SERVICE_UI_ALLOWED フラグを設定すると、メッセージ サービスがインストールされているがその設定を構成するユーザーを有効にすると、プロパティ シートを表示できます。 
  
MapiSvc.inf ファイルには、それぞれのメッセージ サービスとプロパティを構成するプロバイダーの一覧が含まれています。 **CreateMsgServiceEx**は、まずメッセージ サービス用の新しいプロファイル セクションを作成し、そのサービスの情報をすべて MapiSvc.inf ファイルからにコピー、プロファイルでは、プロバイダーごとに新しいセクションを作成します。 
  
MapiSvc.inf からすべての情報がコピーされた後は、 _ulContext_パラメーターに設定された MSG_SERVICE_CREATE 値を持つメッセージ サービスのエントリ ポイント関数、 **MSGSERVICEENTRY**が呼び出されます。 **CreateMsgServiceEx**メソッドの_ulFlags_パラメーターに SERVICE_UI_ALLOWED フラグを設定すると、またには、 _ulUIParam_と_ulFlags_パラメーターの値は、メッセージ サービスのエントリ ポイント関数が呼び出されたときに渡されます。 サービス プロバイダーは、ユーザーは、メッセージ サービスを構成することができますので、構成のプロパティ シートを表示します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CreateMsgServiceEx** _lpuidService_の引数が NULL でない場合は、 **GUID**の指し示す先のプロファイルに追加されたメッセージ サービスの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティが返されます。 
  
**PR_SERVICE_UID**プロパティの値を_lpuidService_パラメーターでメソッドに渡す、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)サービスを構成します。 
  
> [!CAUTION]
> MAPI サブシステムの Microsoft Outlook 2010 の実装は、MAPI_UNICODE をサポートしていませんし、使用されている場合は失敗します。 
  
> [!IMPORTANT]
> IMsgServiceAdmin2 インターフェイスは、IMsgServiceAdmin インターフェイスを実装して、MAPI サブシステムの Outlook 2003 以降の Outlook の実装を使用して提供されている同じオブジェクトによって公開されます。 インターフェイスの IID は、次のように定義されている: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING は、現在あるダウンロード可能なヘッダー ファイルで定義されていない可能性があります、場合に追加できます、次の値を使用してコード: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

