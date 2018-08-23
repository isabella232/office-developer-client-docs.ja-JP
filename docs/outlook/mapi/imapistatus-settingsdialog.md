---
title: IMAPIStatusSettingsDialog
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a21feb474ef69da9ec8e36e06c8649b9d0f93981
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566706"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI が実装している状態のオブジェクトでこのメソッドがサポートされていないサービス ・ プロバイダーの構成を変更するユーザーを有効にするプロパティ シートを表示します。
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]構成のプロパティ シートの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]プロパティ シートの表示を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
UI_READONLY 
  
> プロバイダーをユーザー設定のプロパティを変更するのには有効にする必要があることをお勧めします。 このフラグは、単なる提案です。無視することができます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 構成のプロパティ シートが正常に表示されます。
    
MAPI_E_NO_SUPPORT 
  
> 状態オブジェクトは、このメソッドをサポートしていません**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) のプロパティに STATUS_SETTINGS_DIALOG フラグがない場合で示される。
    
## <a name="remarks"></a>注釈

**IMAPIStatus::SettingsDialog**メソッドでは、[設定] プロパティ シートが表示されます。 すべてのサービス プロバイダーは、 **SettingsDialog**メソッドをサポートする必要がありますが、必須ではありません。 サービス プロバイダーでは、独自のプロパティ シートを実装したり、サポート オブジェクトの[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)メソッドで指定された実装を使用することができます。 **DoConfigPropsheet**は、読み取り/書き込みプロパティ シートを作成します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

リモート トランスポート プロバイダーに設定がある場合は、以下を実行にする必要があります。
  
- トランスポート プロバイダーのプロファイル セクションを開きます。
    
- プロファイルから、トランスポート プロバイダーのプロパティの設定値を取得します。
    
- ダイアログ ボックスでプロパティの設定を表示します。
    
- ダイアログ ボックスは、プロパティの設定の編集を許可している場合は、新しい設定が有効ですし、トランスポート プロバイダーのプロファイル セクションに保存を確認してください。
    
- S_OK、または上記の手順の実行中に返されたエラー値を返します。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

**SettingsDialog**を使用して表示されるプロパティ シートを使用して、さまざまな次のように、タスクを実行できます。 
  
- 既定のメッセージ ストアを指定します。
    
- トランスポートの順番を指定します。
    
- 参照の既定のアドレス帳コンテナーを指定します。
    
- あいまいな名前を解決するための検索順序を指定します。
    
- 既定の個人用アドレス帳を指定します。
    
サービス プロバイダーには、読み取り/書き込み、読み取り専用プロパティ シートまたはプロパティによって、アクセス許可の両方を実装できます。 サービス プロバイダーは、プロパティの制限を設定することにより、個々 のプロパティに異なるアクセス許可を実装できます。 プロパティ シートの既定のモードは、読み取り/書き込みです。 **SettingsDialog**の呼び出しで、UI_READONLY フラグを設定することにより、読み取り専用のプロパティ シートを要求できます。 サービス ・ プロバイダーは読み取り専用のプロパティ シートを実装することはできます。 ただし、一部のサービス プロバイダーは、既定のモードをオーバーライドできません、ためいずれかの種類のプロパティ シートを処理するために準備する必要があります。 
  
ユーザー インターフェイスが常にこの操作の関係を対話型のクライアントのみが**SettingsDialog**を呼び出す必要があります。
  
## <a name="see-also"></a>関連項目



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[PidTagResourceMethods 標準プロパティ](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

