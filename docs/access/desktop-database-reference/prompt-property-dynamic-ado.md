---
title: Prompt プロパティ -- 動的 (ADO)
TOCTitle: Prompt Property--Dynamic (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 723820a2a1c5300bfdc3e688d693d29e2bddda33
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602513"
---
# <a name="prompt-property--dynamic-ado"></a><span data-ttu-id="89356-102">Prompt プロパティ -- 動的 (ADO)</span><span class="sxs-lookup"><span data-stu-id="89356-102">Prompt Property--Dynamic (ADO)</span></span>


<span data-ttu-id="89356-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="89356-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="89356-104">OLE DB プロバイダーから、ユーザーに対して初期化情報を要求するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="89356-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

<span data-ttu-id="89356-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="89356-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="89356-106">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="89356-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="89356-107">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="89356-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="89356-108">master</span><span class="sxs-lookup"><span data-stu-id="89356-108">master</span></span>

<span data-ttu-id="89356-109">[ConnectPromptEnum](connectpromptenum.md) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="89356-109">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89356-110">解説</span><span class="sxs-lookup"><span data-stu-id="89356-110">Remarks</span></span>

<span data-ttu-id="89356-p101">**Prompt** は、OLE DB プロバイダーによって [Connection](connection-object-ado.md) オブジェクトの [Properties](properties-collection-ado.md) コレクションに追加される動的プロパティです。初期化情報を要求する場合、OLE DB プロバイダーは通常、ダイアログ ボックスをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="89356-p101">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider. To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="89356-p102">[Connection](connection-object-ado.md) が閉じると、 **Connection** オブジェクトの動的プロパティは失われます。既定値以外の値を使うには、 **Connection** を再び開く前に **Prompt** プロパティをリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="89356-p102">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed. The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>


> [!NOTE]
> <P><span data-ttu-id="89356-p103">[!メモ] ユーザーがダイアログ ボックスに応答できない状況でプロバイダーからプロンプトを表示するような指定はしないでください。たとえば、アプリケーションを、ユーザーの使用しているクライアント コンピューターではなくサーバー システムで実行している場合や、ユーザーがログオンしていないシステムでアプリケーションが実行されている場合、ユーザーは応答できません。このような状況では、アプリケーションが応答を待って無限に待機することになり、ロックしたような状態になります。</span><span class="sxs-lookup"><span data-stu-id="89356-p103">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box. For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on. In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span></P>



<span data-ttu-id="89356-118">**使用例**</span><span class="sxs-lookup"><span data-stu-id="89356-118">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
