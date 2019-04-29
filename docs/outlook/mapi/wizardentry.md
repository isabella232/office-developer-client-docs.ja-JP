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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430680"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーの構成プロパティシートを表示するのに十分な情報を取得するために、プロファイルウィザードが呼び出すサービスプロバイダーエントリポイント関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiwz  <br/> |
|定義された関数の実装:  <br/> |サービス プロバイダー  <br/> |
|によって呼び出された定義済み関数:  <br/> |MAPI プロファイルウィザード  <br/> |
   
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

 _hproviderdllinstance_
  
> 順番サービスプロバイダーの DLL のインスタンスハンドル。 
    
 _lpcsResourceName_
  
> 読み上げ構成中にプロファイルウィザードによって表示されるダイアログリソースの完全な名前を含む文字列へのポインター。 NULL ターミネータを含む文字列の最大サイズは、32文字です。 
    
 _lppdlgproc_
  
> 読み上げプロファイルウィザードによって呼び出され、さまざまなイベントをプロバイダーに通知する標準の Windows ダイアログボックスプロシージャへのポインター。 
    
 _lpMAPIProp_
  
> 順番構成プロパティへのアクセスを提供するプロパティインターフェイス実装へのポインター。 
    
 _lpMapiSupportObject_
  
> 順番このセッションに適用される MAPI サポートオブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> サービスプロバイダーの**wizardentry**関数が正常に呼び出されました。 
    
MAPI_E_CALL_FAILED 
  
> 予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。
    
## <a name="remarks"></a>注釈

プロファイルウィザードは、サービスプロバイダーの構成ユーザーインターフェイスを表示する準備ができたときに、 **wizardentry**ベースの関数を呼び出します。 すべてのプロバイダーの構成が完了すると、プロファイルウィザードは[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出して、プロファイルに構成プロパティを書き込みます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**wizardentry**に基づく関数の名前は、mapisvc.inf の WIZARD_ENTRY_NAME エントリに配置する必要があります。 
  
リソース名は、プロファイルウィザードのウィンドウに表示されるダイアログリソースの名前です。 渡されるリソースには、1つのダイアログリソース内のすべてのページが含まれている必要があります。 プロファイルウィザードがこのリソースを受け取ると、ダイアログスタイルは無視されますが、コントロールスタイルは無視され、すべてのコントロールがプロファイルウィザードページの子として作成されます。 すべてのコントロールが最初に非表示になります。 プロバイダーは、コントロールの座標が0またはゼロであること、および最大幅が200ダイアログ単位で、最大高さが150ダイアログ単位であることを確認する必要があります。 400の下にあるコントロール id は、プロファイルウィザード用に予約されています。 プロファイルウィザードは、プロバイダーのタイトルを、プロバイダーのユーザーインターフェイスの上に太字のテキストで表示します。 
  
_lpMAPIProp_パラメーターで指定されたプロパティインターフェイスポインターは、プロバイダーが後で参照できるように保持する必要があります。 プロファイルウィザードは、最も基本的なプロパティのセットのみを処理し、プロバイダーはプロパティインターフェイスの実装を使用して、追加のプロパティを含めることができます。 構成時に、プロバイダーは、プロパティインターフェイスを実装するオブジェクトに構成プロパティを追加する必要があります。 すべてのプロバイダーを構成した後、プロファイルウィザードによってこれらのプロパティがプロファイルに追加されます。 
  
この関数の使用方法の詳細については、「[メッセージサービス構成のサポート](supporting-message-service-configuration.md)」を参照してください。 
  

