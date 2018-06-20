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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d80671331c2760c574ab32d79115a352ee4bcf25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801288"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**適用されます**: Outlook 
  
1 つまたは複数のメッセージ サービスをプロファイルに追加するためのプロファイル ウィザード アプリケーションを起動する関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiwz.h  <br/> |
|によって実装される関数の定義:  <br/> |MAPI  <br/> |
|によって呼び出される関数を定義します。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a>Parameters

 _hParentWnd_
  
> [in]呼び出し元の親ウィンドウへのハンドル。 呼び出し元は、親ウィンドウを持たない場合、 _hParentWnd_パラメーターは、NULL のはずです。 
    
 _ulFlags_
  
> [in]プロファイル ウィザードのオプションを示すフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> プロファイル ウィザードでは、 _lppszServiceNameToAdd_パラメーターでは、表示されているメッセージ サービスのみを追加し、メッセージ サービスを選択するためには、そのページを表示できません。 
    
MAPI_PW_FIRST_PROFILE 
  
> プロファイルを作成するのには、このワークステーションの 1 つ目です。 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> メッセージ サービスを選択するためのプロファイル ウィザードのページが表示されない必要があります。 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> プロファイル ウィザードは、コントロール パネルの構成アプリケーションによって起動されました。 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> サービス プロバイダーの構成] ダイアログ ボックスのみを表示する必要があり、プロファイル ウィザードのページは表示されません。 このフラグは、MAPI_PW_ADD_SERVICE_ONLY フラグが設定されている場合にのみ設定できます。 
    
 _lppszServiceNameToAdd_
  
> [in]プロファイルに追加するメッセージ サービスの名前を格納する文字列の配列へのポインター。 配列は NULL 値で終了してください。 
    
 _cbBufferMax_
  
> [in]_LpszNewProfileName_パラメーターが指すバッファーのサイズです。 
    
 _lpszNewProfileName_
  
> [out]作成したプロファイルの名前を**LAUNCHWIZARDENTRY**に基づく関数が返す文字列のバッファーへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。 ダイアログ ボックスから取得する既定のプロファイル、およびエラーにアクセスできない可能性には、プロファイル ウィザードは、MAPI サブシステムを初期化するためにエラーが含まれている。
    
## <a name="remarks"></a>備考

**LAUNCHWIZARDENTRY**関数のプロトタイプの MAPI 実装は、MAPI プロファイル ウィザードのアプリケーションへのエントリ ポイントです。 MAPI では、このエントリ ポイント**LaunchWizard**を名前です。 
  
_UlFlags_パラメーターに MAPI_PW_ADD_SERVICE_ONLY フラグを設定すると、ときに、次の規則が適用されます。 
  
- MAPI_PW_LAUNCHED_BY_CONFIG フラグは、表示されている [ようこそ] ページを禁止します。 
    
- MAPI_PW_HIDE_SERVICES_LIST と MAPI_PW_PROVIDER_UI_ONLY のフラグは、既定のプロファイルがない場合にのみ便利です。 ここではこれらのフラグは、どのプロファイル ウィザードのページが表示されるを確認します。 
    
- 既定のプロファイルが存在する場合、プロファイル ウィザードのページ、表示します。 
    
- 既定のプロファイルが存在する、 _lppszServiceNameToAdd_パラメーターでは、サービスの 1 つのメッセージが表示されているとメッセージ サービスは既に既定のプロファイル、プロファイル ウィザードは、プロファイルに何も追加せず S_OK を返します。 
    
プロファイルに追加するすべてのメッセージ サービスは、プロファイル ウィザードは、 [MSGSERVICEENTRY](msgserviceentry.md)プロトタイプに基づいて、サービスのエントリ ポイント関数を呼び出します。 プロファイルに追加するメッセージ サービスから選択したサービス プロバイダーごとに、プロファイル ウィザードは[WIZARDENTRY](wizardentry.md)プロトタイプに基づいて、プロバイダーのエントリ ポイント関数を呼び出します。 対話型の構成時にプロパティ ページで、すべてのユーザー イベントはプロファイル ウィザードで[SERVICEWIZARDDLGPROC](servicewizarddlgproc.md)プロトタイプに基づいて、プロバイダーのコールバック関数を呼び出すとします。 
  
プロファイルに追加するサービス プロバイダーは、プロファイル ウィザードのページをサポートする場合は、プロファイルのプログラムによる構成を許可する必要があります。
  

