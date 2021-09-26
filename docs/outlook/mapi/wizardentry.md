---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1a61d77c98766acf57bdb24865624023e0145557
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629446"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーの構成プロパティ シートを表示するのに十分な情報を取得するためにプロファイル ウィザードが呼び出すサービス プロバイダー エントリ ポイント関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiwz.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |サービス プロバイダー  <br/> |
|によって呼び出される定義済み関数:  <br/> |MAPI プロファイル ウィザード  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a>パラメーター

 _hProviderDLLInstance_
  
> [in]サービス プロバイダーの DLL のインスタンス ハンドル。 
    
 _lpcsResourceName_
  
> [out]構成時にプロファイル ウィザードによって表示されるダイアログ リソースの完全な名前を含む文字列へのポインター。 NULL ターミネーターを含む文字列の最大サイズは 32 文字です。 
    
 _lppDlgProc_
  
> [out]プロファイル ウィザードによってWindowsさまざまなイベントをプロバイダーに通知するために呼び出される標準のダイアログ ボックス プロシージャへのポインター。 
    
 _lpMAPIProp_
  
> [in]構成プロパティへのアクセスを提供するプロパティ インターフェイス実装へのポインター。 
    
 _lpMapiSupportObject_
  
> [in]このセッションに適用可能な MAPI サポート オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> サービス プロバイダーの **WIZARDENTRY** 関数が正常に呼び出されました。 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。
    
## <a name="remarks"></a>注釈

プロファイル ウィザードは、サービス プロバイダーの構成ユーザー インターフェイスを表示する準備ができたら **、WIZARDENTRY** ベースの関数を呼び出します。 プロファイル ウィザードは、すべてのプロバイダーの構成が完了したら [、IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出して構成プロパティをプロファイルに書き込みます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**WIZARDENTRY ベースの関数** の名前は、MAPISVC.INF の WIZARD_ENTRY_NAMEエントリに配置する必要があります。 
  
リソース名は、プロファイル ウィザードのウィンドウに表示されるダイアログ リソースの名前です。 返されるリソースは、1 つのダイアログ リソース内のすべてのページを含む必要があります。 プロファイル ウィザードがこのリソースを受け取った場合、ダイアログ スタイルは無視されますが、コントロール のスタイルは無視され、[プロファイル ウィザード] ページの子としてすべてのコントロールが作成されます。 すべてのコントロールは、最初は非表示になっています。 プロバイダーは、コントロールの座標が 0 または 0 から始め、最大幅が 200 ダイアログ 単位、最大高さ 150 ダイアログ 単位を超えないようにする必要があります。 400 より下のコントロール識別子は、プロファイル ウィザード用に予約されています。 プロファイル ウィザードは、プロバイダーのユーザー インターフェイスの上に、プロバイダーのタイトルを太字で表示します。 
  
_lpMAPIProp_ パラメーターで指定されたプロパティ インターフェイス ポインターは、将来の参照のためにプロバイダーが保持する必要があります。 プロファイル ウィザードは、最も基本的なプロパティのセットのみを処理し、プロバイダーはプロパティ インターフェイスの実装を使用して追加のプロパティを含めることができます。 構成中に、プロバイダーは、プロパティ インターフェイスを実装するオブジェクトに構成プロパティを追加する必要があります。 すべてのプロバイダーが構成された後、プロファイル ウィザードは、これらのプロパティをプロファイルに追加します。 
  
この関数の使い方の詳細については、「メッセージ サービス構成のサポート [」を参照してください](supporting-message-service-configuration.md)。 
  

