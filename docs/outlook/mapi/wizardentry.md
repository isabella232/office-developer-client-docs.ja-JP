---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2c307d18c5b62e5190aa10632a47a3f16b80e81f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804226"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**適用されます**: Outlook 
  
プロファイル ウィザードは、プロバイダーの構成のプロパティ シートを表示するための十分な情報を取得するためにはサービス プロバイダーのエントリ ポイント関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiwz.h  <br/> |
|によって実装される関数の定義:  <br/> |サービス プロバイダー  <br/> |
|によって呼び出される関数を定義します。  <br/> |MAPI プロファイル ウィザード  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a>Parameters

 _hProviderDLLInstance_
  
> [in]サービス プロバイダーの DLL のインスタンス ハンドルです。 
    
 _lpcsResourceName_
  
> [out]構成中にプロファイル ウィザードによって表示されるダイアログ リソースの完全名を含む文字列へのポインター。 NULL 終端文字を含む、文字列の最大サイズは、32 文字です。 
    
 _lppDlgProc_
  
> [out]標準的な Windows ダイアログ ボックス プロシージャのさまざまなイベント プロバイダーに通知するためにプロファイル ウィザードによって呼び出されるへのポインター。 
    
 _lpMAPIProp_
  
> [in]構成プロパティへのアクセスを提供するプロパティのインターフェイス実装へのポインター。 
    
 _lpMapiSupportObject_
  
> [in]このセッションに適用可能な MAPI のサポートのオブジェクトへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> サービス プロバイダーの**WIZARDENTRY**関数は正常に呼び出されます。 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。
    
## <a name="remarks"></a>備考

プロファイル ウィザードは、サービス プロバイダーの構成のユーザー インターフェイスを表示する準備ができたときに、ベースの**WIZARDENTRY**関数を呼び出します。 プロファイル ウィザードがすべてのプロバイダーの構成が完了すると、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出すことによって、プロファイルに構成プロパティを書き込みます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

MAPISVC.INF の WIZARD_ENTRY_NAME エントリでは、 **WIZARDENTRY**ベースの関数の名前を配置しなければなりません。 
  
ダイアログ リソースのある描画されること、プロファイル ウィザードのウィンドウで、リソースの名前です。 バックさせる必要があります 1 つのダイアログ リソースのすべてのページに渡されるリソースです。 プロファイル ウィザードでは、このリソースを受信すると無視して、ダイアログのスタイルが、コントロール スタイルではありませんし、プロファイル ウィザードのページの子として、すべてのコントロールを作成します。 すべてのコントロールが最初に表示されません。 プロバイダーは、コントロールの座標が 0 であることを確認または 0 から始まる、する必要があり、それらを超えない 200 のダイアログ単位の最大の幅と高さの最大値] ダイアログが 150 単位の。 400 の下のコントロール id は、プロファイル ウィザードの予約されています。 プロファイル ウィザードでは、プロバイダーのユーザー ・ インタ フェース上の太字のテキストで、プロバイダーのタイトルが表示されます。 
  
_LpMAPIProp_パラメーターで指定されたプロパティのインターフェイス ポインターは、将来参照できるように、プロバイダーが保持する必要があります。 プロファイル ウィザードが最も基本的なプロパティのセットだけを扱うし、プロバイダーは、プロパティのインターフェイスの実装を使用して、追加のプロパティが含まれます。 コンフィギュレーションでは、プロバイダーは、プロパティのインターフェイスを実装するオブジェクトへの設定のプロパティを追加する必要があります。 すべてのプロバイダーを構成すると、プロファイル ウィザードはこれらのプロパティをプロファイルに追加します。 
  
この関数を使用する方法の詳細については、[メッセージ サービスの構成のサポート](supporting-message-service-configuration.md)を参照してください。 
  

