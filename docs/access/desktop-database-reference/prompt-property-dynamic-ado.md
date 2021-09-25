---
title: プロンプト動的プロパティ (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 60a6f6e8ea728466648249d9851b1ee326efed74
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577074"
---
# <a name="prompt-dynamic-property-ado"></a>プロンプト動的プロパティ (ADO)

**適用先:** Access 2013、Office 2013

OLE DB プロバイダーから、ユーザーに対して初期化情報を要求するかどうかを指定します。

## <a name="settings-and-return-values"></a>設定および戻り値

[ConnectPromptEnum](connectpromptenum.md) の値を設定または取得します。

## <a name="remarks"></a>注釈

**Prompt** は、OLE DB プロバイダーによって [Connection](connection-object-ado.md) オブジェクトの [Properties](properties-collection-ado.md) コレクションに追加される動的プロパティです。初期化情報を要求する場合、OLE DB プロバイダーは通常、ダイアログ ボックスをユーザーに表示します。

[Connection](connection-object-ado.md) が閉じると、 **Connection** オブジェクトの動的プロパティは失われます。既定値以外の値を使うには、 **Connection** を再び開く前に **Prompt** プロパティをリセットする必要があります。

> [!NOTE]
> [!メモ] ユーザーがダイアログ ボックスに応答できない状況でプロバイダーからプロンプトを表示するような指定はしないでください。たとえば、アプリケーションを、ユーザーの使用しているクライアント コンピューターではなくサーバー システムで実行している場合や、ユーザーがログオンしていないシステムでアプリケーションが実行されている場合、ユーザーは応答できません。このような状況では、アプリケーションが応答を待って無限に待機することになり、ロックしたような状態になります。

**使用例**

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
