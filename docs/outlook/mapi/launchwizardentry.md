---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ed35eabe27223d8c2af6be0a30e6ec678c0dfc8a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584193"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルに 1 つ以上のメッセージ サービスを追加する目的で、プロファイル ウィザード アプリケーションを開始する関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiwz.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |MAPI  <br/> |
|によって呼び出される定義済み関数:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a>パラメーター

 _hParentWnd_
  
> [in]呼び出し元の親ウィンドウへのハンドル。 呼び出し元に親ウィンドウがない場合  _、hParentWnd_ パラメーターは NULL である必要があります。 
    
 _ulFlags_
  
> [in]プロファイル ウィザードのオプションを示すフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> プロファイル ウィザードでは  _、lppszServiceNameToAdd_ パラメーターを使用して一覧表示されているメッセージ サービスのみを追加し、メッセージ サービスを選択するページは表示されません。 
    
MAPI_PW_FIRST_PROFILE 
  
> 作成するプロファイルは、このワークステーションの最初のプロファイルです。 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> メッセージ サービスを選択するプロファイル ウィザードのページは表示されません。 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> プロファイル ウィザードは、コントロール パネル構成アプリケーションによって起動されました。 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> サービス プロバイダーの構成ダイアログ ボックスだけが表示され、プロファイル ウィザードのページは表示されません。 このフラグを設定できるのは、MAPI_PW_ADD_SERVICE_ONLYフラグが設定されている場合のみです。 
    
 _lppszServiceNameToAdd_
  
> [in]プロファイルに追加するメッセージ サービスの名前を含む文字列の配列へのポインター。 配列は NULL 値で終了する必要があります。 
    
 _cbBufferMax_
  
> [in]  _lpszNewProfileName_ パラメーターが指すバッファーのサイズ。 
    
 _lpszNewProfileName_
  
> [out] **LAUNCHWIZARDENTRY** に基づく関数が作成されたプロファイルの名前を返す文字列バッファーへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。 プロファイル ウィザードの MAPI サブシステムの初期化に失敗した場合、既定のプロファイルにアクセスできません。ダイアログ ボックスからエラーが返される可能性があります。
    
## <a name="remarks"></a>注釈

**LAUNCHWIZARDENTRY** 関数プロトタイプの MAPI 実装は、MAPI プロファイル ウィザード アプリケーションへのエントリ ポイントです。 MAPI の名前は、このエントリ ポイント **LaunchWizard です**。 
  
_ulFlags_ パラメーター MAPI_PW_ADD_SERVICE_ONLYフラグが設定されている場合、次のルールが適用されます。 
  
- このMAPI_PW_LAUNCHED_BY_CONFIGは、ウェルカム ページの表示を禁止します。 
    
- 既定MAPI_PW_HIDE_SERVICES_LISTおよびMAPI_PW_PROVIDER_UI_ONLYフラグは、既定のプロファイルがない場合にのみ役立ちます。 この場合、これらのフラグは、表示するプロファイル ウィザード ページを決定します。 
    
- 既定のプロファイルが存在する場合、どのプロファイル ウィザード ページも表示されません。 
    
- 既定のプロファイルが存在する場合  _、lppszServiceNameToAdd_ パラメーターを使用して 1 つのメッセージ サービスだけが一覧表示され、そのメッセージ サービスは既定のプロファイルに既に存在し、プロファイル ウィザードはプロファイルに何も追加せずに S_OK を返します。 
    
プロファイルに追加するメッセージ サービスごとに、プロファイル ウィザードは [MSGSERVICEENTRY](msgserviceentry.md) プロトタイプに基づいてサービスのエントリ ポイント関数を呼び出します。 プロファイルに追加するメッセージ サービスから選択された各サービス プロバイダーについて、プロファイル ウィザードは WIZARDENTRY プロトタイプに基づいてプロバイダーのエントリ ポイント関数 [を呼び出](wizardentry.md) します。 対話型構成中に、プロパティ ページ内のすべてのユーザー イベントによって、プロファイル ウィザードは [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) プロトタイプに基づいてプロバイダーのコールバック関数を呼び出します。 
  
プロファイルに追加するサービス プロバイダーがプロファイル ウィザード ページをサポートしている場合は、プロファイルのプログラムによる構成を許可する必要があります。
  

