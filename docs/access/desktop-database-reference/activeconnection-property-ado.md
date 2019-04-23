---
title: ActiveConnection プロパティ (ADO)
TOCTitle: ActiveConnection property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 10/17/2018
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 037ae753f427c42f147972170dbb2e645b260623
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282531"
---
# <a name="activeconnection-property-ado"></a><span data-ttu-id="20733-102">ActiveConnection プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="20733-102">ActiveConnection property (ADO)</span></span>

<span data-ttu-id="20733-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="20733-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20733-104">指定された [Command](connection-object-ado.md) オブジェクト、 [Recordset](command-object-ado.md) オブジェクト、または [Record](recordset-object-ado.md) オブジェクトが現在属している [Connection](record-object-ado.md) オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="20733-104">Indicates to which [Connection](connection-object-ado.md) object the specified [Command](command-object-ado.md), [Recordset](recordset-object-ado.md), or [Record](record-object-ado.md) object currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="20733-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="20733-105">Settings and return values</span></span>

<span data-ttu-id="20733-p101">接続が閉じている場合には接続の定義が格納された文字列型 ( **String** ) の値を、接続が開いている場合には現在の **Connection** オブジェクトが格納されたバリアント型 ( **Variant** ) の値を設定または取得します。既定は、Null オブジェクト参照です。 [ConnectionString](connectionstring-property-ado.md) プロパティの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20733-p101">Sets or returns a **String** value that contains a definition for a connection if the connection is closed, or a **Variant** containing the current **Connection** object if the connection is open. Default is a null object reference. See the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="20733-109">注釈</span><span class="sxs-lookup"><span data-stu-id="20733-109">Remarks</span></span>

<span data-ttu-id="20733-110">**ActiveConnection** プロパティを使用すると、指定された **Command** オブジェクトを実行する、または指定された **Recordset** を開く **Connection** オブジェクトを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="20733-110">Use the **ActiveConnection** property to determine the **Connection** object over which the specified **Command** object will execute or the specified **Recordset** will be opened.</span></span>

### <a name="command"></a><span data-ttu-id="20733-111">Command</span><span class="sxs-lookup"><span data-stu-id="20733-111">Command</span></span>

<span data-ttu-id="20733-112">**Command** オブジェクトの場合、**ActiveConnection** プロパティは値の設定も取得も可能です。</span><span class="sxs-lookup"><span data-stu-id="20733-112">For **Command** objects, the **ActiveConnection** property is read/write.</span></span>

<span data-ttu-id="20733-113">開いている [Connection](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) オブジェクトまたは有効な接続文字列をこのプロパティに設定する前に、 **Command** オブジェクトに対して **Execute** を呼び出そうとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20733-113">If you attempt to call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method on a **Command** object before setting this property to an open **Connection** object or valid connection string, an error occurs.</span></span>

<span data-ttu-id="20733-114">**Microsoft Visual Basic**: **ActiveConnection**プロパティを*Nothing*に設定すると、現在の**接続**から**Command**オブジェクトを切り離し、プロバイダーがデータに関連付けられているリソースを解放します。ソース.</span><span class="sxs-lookup"><span data-stu-id="20733-114">**Microsoft Visual Basic**: Setting the **ActiveConnection** property to *Nothing* disassociates the **Command** object from the current **Connection** and causes the provider to release any associated resources on the data source.</span></span> <span data-ttu-id="20733-115">その後は、その **Command** オブジェクトを同じまたは別の **Connection** オブジェクトに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="20733-115">You can then associate the **Command** object with the same or another **Connection** object.</span></span> <span data-ttu-id="20733-116">プロバイダーによっては、プロパティを*Nothing*に設定しなくても、ある接続から別の**接続**にプロパティ設定を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="20733-116">Some providers allow you to change the property setting from one **Connection** to another, without having to first set the property to *Nothing*.</span></span>

<span data-ttu-id="20733-p103">**Command** オブジェクトの [Parameters](parameters-collection-ado.md) コレクションにプロバイダーから供給されたパラメーターが格納されている場合は、**ActiveConnection** プロパティを *Nothing* に設定したり、他の **Connection** オブジェクトに設定したりすると、コレクションがクリアされます。手作業で [Parameter](parameter-object-ado.md) オブジェクトを作成し、それを使用して **Command** オブジェクトの **Parameters** コレクションにデータを格納した場合は、**ActiveConnection** プロパティを *Nothing* や他の **Connection** オブジェクトに設定しても、**Parameters** コレクションはそのまま残されます。</span><span class="sxs-lookup"><span data-stu-id="20733-p103">If the [Parameters](parameters-collection-ado.md) collection of the **Command** object contains parameters supplied by the provider, the collection is cleared if you set the **ActiveConnection** property to *Nothing* or to another **Connection** object. If you manually create [Parameter](parameter-object-ado.md) objects and use them to fill the **Parameters** collection of the **Command** object, setting the **ActiveConnection** property to *Nothing* or to another **Connection** object leaves the **Parameters** collection intact.</span></span>

<span data-ttu-id="20733-p104">**Command** オブジェクトが関連付けられている **Connection** オブジェクトを閉じると、**ActiveConnection** プロパティが *Nothing* に設定されます。このプロパティに閉じている **Connection** オブジェクトを設定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="20733-p104">Closing the **Connection** object with which a **Command** object is associated sets the **ActiveConnection** property to *Nothing*. Setting this property to a closed **Connection** object generates an error.</span></span>

### <a name="recordset"></a><span data-ttu-id="20733-121">Recordset</span><span class="sxs-lookup"><span data-stu-id="20733-121">Recordset</span></span>

<span data-ttu-id="20733-p105">開いている **Recordset** オブジェクト、および **Source** プロパティが有効な [Command](source-property-ado-recordset.md) オブジェクトに設定されている **Recordset** オブジェクトについては、 **ActiveConnection** プロパティは値の取得のみ可能です。それ以外の場合は、値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="20733-p105">For open **Recordset** objects or for **Recordset** objects whose [Source](source-property-ado-recordset.md) property is set to a valid **Command** object, the **ActiveConnection** property is read-only. Otherwise, it is read/write.</span></span>

<span data-ttu-id="20733-p106">このプロパティは、有効な **Connection** オブジェクトまたは有効な接続文字列に設定できます。この場合、プロバイダーが、この定義を使用して新しい **Connection** オブジェクトを作成し、接続を開きます。さらに、プログラマが **Connection** オブジェクトにアクセスして拡張エラー情報を取得したり、その他のコマンドを実行したりできるように、プロバイダーがこのプロパティを新しい **Connection** オブジェクトに設定する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="20733-p106">You can set this property to a valid **Connection** object or to a valid connection string. In this case, the provider creates a new **Connection** object using this definition and opens the connection. Additionally, the provider may set this property to the new **Connection** object to give you a way to access the **Connection** object for extended error information or to execute other commands.</span></span>

<span data-ttu-id="20733-127">[Open](open-method-ado-recordset.md) メソッドの *ActiveConnection* 引数を使用して **Recordset** オブジェクトを開いた場合、**ActiveConnection** プロパティは引数の値を継承します。</span><span class="sxs-lookup"><span data-stu-id="20733-127">If you use the *ActiveConnection* argument of the [Open](open-method-ado-recordset.md) method to open a **Recordset** object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="20733-128">**Recordset** オブジェクトの **Source** プロパティを有効な **Command** オブジェクト変数に設定すると、**Recordset** の **ActiveConnection** プロパティは、**Command** オブジェクトの **ActiveConnection** プロパティの値を継承します。</span><span class="sxs-lookup"><span data-stu-id="20733-128">If you set the **Source** property of the **Recordset** object to a valid **Command** object variable, the **ActiveConnection** property of the **Recordset** inherits the setting of the **Command** object's **ActiveConnection** property.</span></span>

<span data-ttu-id="20733-129">**リモートデータサービスの使用法**: クライアント側の Recordset オブジェクトで使用されている場合、このプロパティは、接続文字列または (Microsoft visual basic または visual basic, Scripting Edition では) *Nothing*にのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="20733-129">**Remote Data Service Usage**: When used on a client-side Recordset object, this property can be set only to a connection string or (in Microsoft Visual Basic or Visual Basic, Scripting Edition) to *Nothing*.</span></span>

### <a name="record"></a><span data-ttu-id="20733-130">Record</span><span class="sxs-lookup"><span data-stu-id="20733-130">Record</span></span>

<span data-ttu-id="20733-p107">このプロパティは、**Record** オブジェクトが閉じている場合には値の設定および取得が可能で、接続文字列または開いている **Connection** オブジェクトの参照を格納できます。**Record** オブジェクトが開いている場合は値の取得のみ可能で、開いている **Connection** オブジェクトの参照が格納されています。</span><span class="sxs-lookup"><span data-stu-id="20733-p107">This property is read/write when the **Record** object is closed, and may contain a connection string or reference to an open **Connection** object. This property is read-only when the **Record** object is open, and contains a reference to an open **Connection** object.</span></span>

<span data-ttu-id="20733-133">**Connection** オブジェクトは、URL から **Record** オブジェクトが開かれたときに暗黙的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="20733-133">A **Connection** object is created implicitly when the **Record** object is opened from a URL.</span></span> <span data-ttu-id="20733-134">既存の、開いている **Connection** オブジェクトで **Record** を開くには、 **Connection** オブジェクトをこのプロパティに代入するか、または **Connection** オブジェクトを [Open](open-method-ado-record.md) メソッド呼び出しのパラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="20733-134">Open the **Record** with an existing, open **Connection** object by assigning the **Connection** object to this property, or using the **Connection** object as a parameter in the [Open](open-method-ado-record.md) method call.</span></span> <span data-ttu-id="20733-135">**record**を既存の**record**または[recordset](recordset-object-ado.md)から開いた場合は、そのレコードまたは\*\*\*\* **recordset**オブジェクトの**Connection**オブジェクトに自動的に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="20733-135">If the **Record** is opened from an existing **Record** or [Recordset](recordset-object-ado.md), it is automatically associated with that **Record** or **Recordset** object's **Connection** object.</span></span>

> [!NOTE]
> <span data-ttu-id="20733-136">[!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="20733-136">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="20733-137">詳細については、「[絶対 url と相対 url](absolute-and-relative-urls.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20733-137">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>



