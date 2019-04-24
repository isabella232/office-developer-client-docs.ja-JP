---
title: imapistatussettingsdialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331543"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーがサービスプロバイダーの構成を変更できるようにするプロパティシートを表示します。このメソッドは、MAPI が実装する status オブジェクトではサポートされていません。
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番構成プロパティシートの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> 順番プロパティシートの表示を制御するフラグのビットマスク。 次のフラグを設定できます。
    
UI_READONLY 
  
> プロバイダーが、ユーザーが構成プロパティを変更できないようにすることを提案します。 このフラグは、提案のみです。無視できます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 構成プロパティシートが正常に表示されました。
    
MAPI_E_NO_SUPPORT 
  
> status オブジェクトは、 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティの STATUS_SETTINGS_DIALOG フラグが指定されていないため、このメソッドをサポートしていません。
    
## <a name="remarks"></a>解説

**imapistatus:: settingsdialog**メソッドは、構成プロパティシートを表示します。 すべてのサービスプロバイダーは**settingsdialog**メソッドをサポートする必要がありますが、必須ではありません。 サービスプロバイダーは、独自のプロパティシートを実装するか、support オブジェクトの[imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)メソッドで提供される実装を使用できます。 **doconfigpropsheet**は、読み取り/書き込み可能なプロパティシートを作成します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

リモートトランスポートプロバイダーに設定がある場合は、次の操作を実行する必要があります。
  
- [トランスポートプロバイダーのプロファイル] セクションを開きます。
    
- プロファイルからトランスポートプロバイダーのプロパティ設定を取得します。
    
- プロパティの設定をダイアログボックスに表示します。
    
- ダイアログボックスでプロパティの設定を編集できる場合は、新しい設定が有効になっていることを確認し、それをトランスポートプロバイダーの [プロファイル] セクションに保存します。
    
- S_OK、または前の手順で返されたエラー値を返します。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

**settingsdialog**を使用して表示されるプロパティシートを使用して、次のようなさまざまなタスクを実行できます。 
  
- 既定のメッセージストアを指定します。
    
- トランスポート順序を指定します。
    
- 参照用の既定のアドレス帳コンテナーを指定します。
    
- あいまいな名前を解決するための検索順序を指定します。
    
- 既定の個人用アドレス帳を指定します。
    
サービスプロバイダーは、プロパティに応じて、読み取り/書き込み可能なプロパティシート、読み取り専用の権限、または複数の権限を組み合わせて実装することができます。 サービスプロバイダーは、プロパティ制限を設定することによって、個々のプロパティに対して異なる権限を実装できます。 プロパティシートの既定のモードは、値の取得および設定が可能です。 読み取り専用のプロパティシートを要求するには、 **settingsdialog**の呼び出しで UI_READONLY フラグを設定します。 読み取り専用のプロパティシートを実装できるサービスプロバイダーは、これを行うことができます。 ただし、一部のサービスプロバイダーは既定のモードを上書きできないため、どちらかの種類のプロパティシートを処理できるように準備しておく必要があります。 
  
ユーザーインターフェイスは常にこの操作に関係するため、interactive クライアントだけが**settingsdialog**を呼び出す必要があります。
  
## <a name="see-also"></a>関連項目



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[PidTagResourceMethods 標準プロパティ](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

