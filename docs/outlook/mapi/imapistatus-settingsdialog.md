---
title: IMAPIStatusSettingsDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d38a9930e9bdd3fcc5fb782c5bec45b1b6147e2e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567502"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーがサービス プロバイダーの構成を変更できるプロパティ シートを表示しますこのメソッドは、MAPI が実装する状態オブジェクトではサポートされていません。
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]構成プロパティ シートの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]プロパティ シートの表示を制御するフラグのビットマスク。 次のフラグを設定できます。
    
UI_READONLY 
  
> プロバイダーは、構成プロパティを変更するユーザーを有効にしない必要があります。 このフラグは、提案にすすむのみです。無視できます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 構成プロパティ シートが正常に表示されました。
    
MAPI_E_NO_SUPPORT 
  
> status オブジェクトは、PR_RESOURCE_METHODS ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_SETTINGS_DIALOG フラグがない場合 **に** 示されるこのメソッドをサポートします。
    
## <a name="remarks"></a>注釈

**IMAPIStatus::SettingsDialog** メソッドは、構成プロパティ シートを表示します。 すべてのサービス プロバイダーは **SettingsDialog メソッドをサポートする必要** がありますが、必須ではありません。 サービス プロバイダーは、独自のプロパティ シートを実装するか、サポート オブジェクトの [IMAPISupport::D oConfigPropsheet メソッドで提供される実装を使用](imapisupport-doconfigpropsheet.md) できます。 **DoConfigPropsheet は** 、読み取り/書き込みプロパティ シートを作成します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

リモート トランスポート プロバイダーに設定がある場合は、次の操作を行う必要があります。
  
- トランスポート プロバイダーのプロファイル セクションを開きます。
    
- プロファイルからトランスポート プロバイダーのプロパティ設定を取得します。
    
- ダイアログ ボックスにプロパティ設定を表示します。
    
- ダイアログ ボックスでプロパティ設定の編集が許可されている場合は、新しい設定が有効か確認し、トランスポート プロバイダーのプロファイル セクションに保存します。
    
- 前S_OKエラー値を返します。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

**SettingsDialog** で表示されるプロパティ シートを使用すると、次のようなさまざまなタスクを実行できます。 
  
- 既定のメッセージ ストアを指定します。
    
- トランスポートの順序を指定します。
    
- 参照用の既定のアドレス帳コンテナーを指定します。
    
- あいまいな名前を解決するための検索順序を指定します。
    
- 既定の個人用アドレス帳を指定します。
    
サービス プロバイダーは、プロパティに応じて、読み取り/書き込み、読み取り専用、または複数のアクセス許可を含むプロパティ シートを実装できます。 サービス プロバイダーは、プロパティの制限を設定することで、個々のプロパティに対して異なるアクセス許可を実装できます。 プロパティ シートの既定のモードは読み取り/書き込みです。 SettingsDialog の呼び出しで UI_READONLYフラグを設定することで、読み取り専用のプロパティ シート **を要求できます**。 読み取り専用のプロパティ シートを実装できるサービス プロバイダーは、これを実行できます。 ただし、一部のサービス プロバイダーは既定のモードを上書きできないので、いずれかの種類のプロパティ シートを処理する準備が必要です。 
  
ユーザー インターフェイスは常にこの操作に関与しますので、対話的なクライアントだけが **SettingsDialog を呼び出す必要があります**。
  
## <a name="see-also"></a>関連項目



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[PidTagResourceMethods 標準プロパティ](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

