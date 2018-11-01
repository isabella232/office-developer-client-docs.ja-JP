---
title: Prompt プロパティ -- 動的 (ADO)
TOCTitle: Prompt Property--Dynamic (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 491aea720995ec140ef3701a5ffdbdc5171c4a32
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868358"
---
# <a name="prompt-property--dynamic-ado"></a><span data-ttu-id="c5607-102">Prompt プロパティ -- 動的 (ADO)</span><span class="sxs-lookup"><span data-stu-id="c5607-102">Prompt Property--Dynamic (ADO)</span></span>


<span data-ttu-id="c5607-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c5607-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5607-104">OLE DB プロバイダーから、ユーザーに対して初期化情報を要求するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c5607-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c5607-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="c5607-105">Settings and return values</span></span>

<span data-ttu-id="c5607-106">[ConnectPromptEnum](connectpromptenum.md) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="c5607-106">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5607-107">解説</span><span class="sxs-lookup"><span data-stu-id="c5607-107">Remarks</span></span>

<span data-ttu-id="c5607-p101">**Prompt** は、OLE DB プロバイダーによって [Connection](connection-object-ado.md) オブジェクトの [Properties](properties-collection-ado.md) コレクションに追加される動的プロパティです。初期化情報を要求する場合、OLE DB プロバイダーは通常、ダイアログ ボックスをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="c5607-p101">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider. To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="c5607-p102">[Connection](connection-object-ado.md) が閉じると、 **Connection** オブジェクトの動的プロパティは失われます。既定値以外の値を使うには、 **Connection** を再び開く前に **Prompt** プロパティをリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5607-p102">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed. The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c5607-p103">[!メモ] ユーザーがダイアログ ボックスに応答できない状況でプロバイダーからプロンプトを表示するような指定はしないでください。たとえば、アプリケーションを、ユーザーの使用しているクライアント コンピューターではなくサーバー システムで実行している場合や、ユーザーがログオンしていないシステムでアプリケーションが実行されている場合、ユーザーは応答できません。このような状況では、アプリケーションが応答を待って無限に待機することになり、ロックしたような状態になります。</span><span class="sxs-lookup"><span data-stu-id="c5607-p103">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box. For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on. In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span></P>



<span data-ttu-id="c5607-115">**使用例**</span><span class="sxs-lookup"><span data-stu-id="c5607-115">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
