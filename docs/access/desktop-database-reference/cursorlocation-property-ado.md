---
title: CursorLocation プロパティ (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 874662585292b9d9a9b2bc53f5b6fe5178e3517b
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025848"
---
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="72961-102">CursorLocation プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="72961-102">CursorLocation property (ADO)</span></span>


<span data-ttu-id="72961-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="72961-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72961-104">カーソル サービスの場所を示します。</span><span class="sxs-lookup"><span data-stu-id="72961-104">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="72961-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="72961-105">Settings And Return Values</span></span>

<span data-ttu-id="72961-106">**CursorLocationEnum** 値のいずれか 1 つに設定可能な長整数型 ( [Long](cursorlocationenum.md) ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="72961-106">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="72961-107">解説</span><span class="sxs-lookup"><span data-stu-id="72961-107">Remarks</span></span>

<span data-ttu-id="72961-p101">このプロパティで、プロバイダーにアクセス可能なさまざまなカーソル ライブラリの中からカーソル サービスを選択します。通常は、クライアント側カーソル ライブラリ、またはサーバー側カーソル ライブラリから選択します。</span><span class="sxs-lookup"><span data-stu-id="72961-p101">This property allows you to choose between various cursor libraries accessible to the provider. Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="72961-p102">このプロパティ設定は、プロパティが設定された後に確立された接続のみに作用します。 **CursorLocation** プロパティを変更しても既存の接続には影響しません。</span><span class="sxs-lookup"><span data-stu-id="72961-p102">This property setting affects connections established only after the property has been set. Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="72961-p103">[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) メソッドが返すカーソルは、この設定を継承します。 **Recordset** オブジェクトは、関連付けられた接続からこの設定を自動的に継承します。</span><span class="sxs-lookup"><span data-stu-id="72961-p103">Cursors returned by the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method inherit this setting. **Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="72961-114">このプロパティは、[Connection](connection-object-ado.md) または閉じている [Recordset](recordset-object-ado.md) 上では読み取り/書き込み可能ですが、開いている **Recordset** 上では読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="72961-114">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="72961-115">**リモート データ サービスの使用法**使用すると、クライアント側の**レコード セット**または**接続**オブジェクトの**CursorLocation**プロパティは**adUseClient**にのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="72961-115">**Remote Data Service Usage**When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

