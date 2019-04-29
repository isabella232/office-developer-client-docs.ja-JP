---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437386"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルに1つ以上のメッセージサービスを追加することを目的として、プロファイルウィザードアプリケーションを起動する関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiwz  <br/> |
|定義された関数の実装:  <br/> |MAPI  <br/> |
|によって呼び出された定義済み関数:  <br/> |クライアント アプリケーション  <br/> |
   
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
  
> 順番呼び出し元の親ウィンドウへのハンドル。 呼び出し元が親ウィンドウを持たない場合は、 _hParentWnd_パラメーターを NULL にする必要があります。 
    
 _ulFlags_
  
> 順番プロファイルウィザードのオプションを示すフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> プロファイルウィザードでは、 _lppszServiceNameToAdd_パラメーターを使用してメッセージサービスのみを追加し、メッセージサービスを選択するためのページを表示しないようにします。 
    
MAPI_PW_FIRST_PROFILE 
  
> このワークステーションの最初のプロファイルが作成されます。 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> メッセージサービスを選択するためのプロファイルウィザードのページは表示されません。 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> プロファイルウィザードは、コントロールパネル構成アプリケーションによって起動されました。 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> サービスプロバイダーの [構成] ダイアログボックスだけが表示され、プロファイルウィザードのページは表示されません。 このフラグは、MAPI_PW_ADD_SERVICE_ONLY フラグが設定されている場合にのみ設定できます。 
    
 _lppszServiceNameToAdd_
  
> 順番プロファイルに追加するメッセージサービスの名前を含む文字列の配列へのポインター。 配列は NULL 値で終了する必要があります。 
    
 _cbbuffermax_
  
> 順番_lpsznewprofilename_パラメーターによって示されるバッファーのサイズ。 
    
 _lpsznewprofilename_
  
> 読み上げ**launchwizardentry**に基づく関数が、作成されたプロファイルの名前を返す文字列バッファーへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。 これには、プロファイルウィザードの MAPI サブシステムを初期化できない、既定のプロファイルにアクセスできない、およびダイアログボックスからエラーが返されるなどの可能性があります。
    
## <a name="remarks"></a>注釈

**launchwizardentry**関数プロトタイプの mapi 実装は、mapi プロファイルウィザードアプリケーションへのエントリポイントです。 [MAPI 名] このエントリポイントの**launchwizard**。 
  
_ulflags_パラメーターに MAPI_PW_ADD_SERVICE_ONLY フラグが設定されている場合は、次のルールが適用されます。 
  
- MAPI_PW_LAUNCHED_BY_CONFIG フラグは、ウェルカムページが表示されないようにします。 
    
- MAPI_PW_HIDE_SERVICES_LIST および MAPI_PW_PROVIDER_UI_ONLY フラグは、既定のプロファイルがない場合にのみ役立ちます。 この場合、次のフラグは、どのプロファイルウィザードページを表示するかを決定します。 
    
- 既定のプロファイルが存在する場合、プロファイルウィザードページは表示されません。 
    
- 既定のプロファイルが存在する場合、 _lppszServiceNameToAdd_パラメーターによって表示されるメッセージサービスは1つだけで、そのメッセージサービスは既に既定のプロファイルになっています。プロファイルウィザードは、プロファイルに何も追加せずに S_OK を返します。 
    
プロファイルに追加されるすべてのメッセージサービスについて、プロファイルウィザードは[msgserviceentry](msgserviceentry.md)プロトタイプに基づいてサービスのエントリポイント関数を呼び出します。 プロファイルに追加するメッセージサービスから選択された各サービスプロバイダーについて、プロファイルウィザードは、 [wizardentry](wizardentry.md) prototype に基づいて、プロバイダーのエントリポイント関数を呼び出します。 対話形式の構成では、プロパティページのすべてのユーザーイベントによって、プロファイルウィザードによって、 [servicewizarddlgproc](servicewizarddlgproc.md)プロトタイプに基づいてプロバイダーのコールバック関数が呼び出されます。 
  
プロファイルに追加されるサービスプロバイダーがプロファイルウィザードページをサポートしている場合は、プロファイルのプログラムによる構成を許可する必要があります。
  

