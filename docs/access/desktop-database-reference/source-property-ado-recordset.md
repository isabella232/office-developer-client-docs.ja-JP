---
title: Source プロパティ (ADO Recordset)
TOCTitle: Source Property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db44459bf3629f6cedfbee023b0be9161ed3bb14
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605262"
---
# <a name="source-property-ado-recordset"></a><span data-ttu-id="d0ee4-102">Source プロパティ (ADO Recordset)</span><span class="sxs-lookup"><span data-stu-id="d0ee4-102">Source Property (ADO Recordset)</span></span>


<span data-ttu-id="d0ee4-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0ee4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d0ee4-104">[Recordset](recordset-object-ado.md) オブジェクトのデータ ソースを示します。</span><span class="sxs-lookup"><span data-stu-id="d0ee4-104">Indicates the data source for a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="d0ee4-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="d0ee4-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="d0ee4-106">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="d0ee4-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="d0ee4-107">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="d0ee4-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="d0ee4-108">master</span><span class="sxs-lookup"><span data-stu-id="d0ee4-108">master</span></span>

<span data-ttu-id="d0ee4-109">文字列型 ( **String** ) の値または [Command](command-object-ado.md) オブジェクトへの参照を設定し、 **Recordset** のソースを示す文字列型 ( **String** ) の値のみを返します。</span><span class="sxs-lookup"><span data-stu-id="d0ee4-109">Sets a **String** value or [Command](command-object-ado.md) object reference; returns only a **String** value that indicates the source of the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0ee4-110">解説</span><span class="sxs-lookup"><span data-stu-id="d0ee4-110">Remarks</span></span>

<span data-ttu-id="d0ee4-111">**Command** オブジェクト変数、SQL ステートメント、ストアド プロシージャ、またはテーブル名のいずれかを使用して、 **Recordset** オブジェクトのデータ ソースを指定するには、 **Source** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d0ee4-111">Use the **Source** property to specify a data source for a **Recordset** object using one of the following: a **Command** object variable, an SQL statement, a stored procedure, or a table name.</span></span>

<span data-ttu-id="d0ee4-p101">**Source** プロパティを **Command** オブジェクトに設定した場合、 [Recordset](activeconnection-property-ado.md) オブジェクトの **ActiveConnection** プロパティは、指定した **Command** オブジェクトの **ActiveConnection** プロパティの値を継承します。ただし、 **Source** プロパティの値を取得しても **Command** オブジェクトは返されず、代わりに [Source](commandtext-property-ado.md) プロパティで設定した **Command** オブジェクトの **CommandText** プロパティが返されます。</span><span class="sxs-lookup"><span data-stu-id="d0ee4-p101">If you set the **Source** property to a **Command** object, the [ActiveConnection](activeconnection-property-ado.md) property of the **Recordset** object will inherit the value of the **ActiveConnection** property for the specified **Command** object. However, reading the **Source** property does not return a **Command** object; instead, it returns the [CommandText](commandtext-property-ado.md) property of the **Command** object to which you set the **Source** property.</span></span>

<span data-ttu-id="d0ee4-114">**Source**プロパティが、SQL ステートメント、ストアド プロシージャ、またはテーブル名の場合は、 [Open](open-method-ado-recordset.md)メソッドの呼び出しで適切な*Options*引数を渡すことによってパフォーマンスを最適化できます。</span><span class="sxs-lookup"><span data-stu-id="d0ee4-114">If the **Source** property is an SQL statement, a stored procedure, or a table name, you can optimize performance by passing the appropriate *Options* argument with the [Open](open-method-ado-recordset.md) method call.</span></span>

<span data-ttu-id="d0ee4-115">**Source** プロパティは、 **Recordset** オブジェクトが閉じている場合は値の取得および設定が可能で、 **Recordset** オブジェクトが開いている場合は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="d0ee4-115">The **Source** property is read/write for closed **Recordset** objects and read-only for open **Recordset** objects.</span></span>

