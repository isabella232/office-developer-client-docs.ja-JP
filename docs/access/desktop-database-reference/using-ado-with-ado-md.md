---
title: ADO と ADO MD を共に使用する
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 80c87f57a96f98de704e3cfa9b7689a522e4a7af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312748"
---
# <a name="using-ado-with-ado-md"></a><span data-ttu-id="6c0b3-102">ADO MD を用いた ADO の使用</span><span class="sxs-lookup"><span data-stu-id="6c0b3-102">Using ADO with ADO MD</span></span>


<span data-ttu-id="6c0b3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c0b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c0b3-p101">ADO と ADO MD は関連はしていますが、別々のオブジェクト モデルです。ADO には、データ ソースへの接続、コマンドの実行、表形式のデータと表形式のスキーマ メタデータの取得、およびプロバイダーのエラー情報を表示するためのオブジェクトが用意されています。ADO MD には、多次元データの取得、および多次元スキーマ メタデータの表示のためのオブジェクトが用意されています。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-p101">ADO and ADO MD are related but separate object models. ADO provides objects for connecting to data sources, executing commands, retrieving tabular data and schema metadata in a tabular format, and viewing provider error information. ADO MD provides objects for retrieving multidimensional data and viewing multidimensional schema metadata.</span></span>

<span data-ttu-id="6c0b3-p102">MDP で作業する場合、作成するアプリケーションでは、ADO、ADO MD、またはその両方を選択できます。プロジェクトから両方のライブラリを参照することにより、MDP で提供されるすべての機能に完全にアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-p102">When working with an MDP you may choose to use ADO, ADO MD, or both with your application. By referencing both libraries within your project, you will have full access to the functionality provided by your MDP.</span></span>

<span data-ttu-id="6c0b3-109">多次元データセットを単層化した表形式で表示できることは、便利な場合があります。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-109">It is often useful for consumers to get a flattened, tabular view of a multidimensional dataset.</span></span> <span data-ttu-id="6c0b3-110">これを行うには、ADO の [Recordset](recordset-object-ado.md) オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-110">You can do this by using the ADO [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="6c0b3-111">[Cellset オブジェクト](cellset-object-ado-md.md)のソースを指定する場合、ADO MD ***Cellset*** のソースとしてではなく、**Recordset** の Open メソッドの **[Source](open-method-ado-recordset.md)** パラメーターとして指定します。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-111">Specify the source for your [Cellset](cellset-object-ado-md.md) as the ***Source*** parameter for the [Open](open-method-ado-recordset.md) method of a **Recordset**, rather than as the source for an ADO MD **Cellset**.</span></span>

<span data-ttu-id="6c0b3-112">また、オブジェクトの階層としてではなく、表形式のビューでスキーマのメタデータを表示すると便利な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-112">It may also be useful to view the schema metadata in a tabular view rather than as a hierarchy of objects.</span></span> <span data-ttu-id="6c0b3-113">[Connection](connection-object-ado.md)オブジェクトの ADO [OpenSchema](openschema-method-ado.md)メソッドを使用すると、ユーザーはスキーマ情報を含む**Recordset**を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-113">The ADO [OpenSchema](openschema-method-ado.md) method on the [Connection](connection-object-ado.md) object allows the user to open a **Recordset** containing schema information.</span></span> <span data-ttu-id="6c0b3-114">**OpenSchema**メソッドの***QueryType***パラメーターには、mdps に特に関連する複数の[schemaenum](schemaenum.md)値があります。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-114">The ***QueryType*** parameter of the **OpenSchema** method has several [SchemaEnum](schemaenum.md) values that relate specifically to MDPs.</span></span> <span data-ttu-id="6c0b3-115">これらの値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-115">These values are:</span></span>

  - <span data-ttu-id="6c0b3-116">**adSchemaCubes**</span><span class="sxs-lookup"><span data-stu-id="6c0b3-116">**adSchemaCubes**</span></span>

  - <span data-ttu-id="6c0b3-117">**adschemadimensions**</span><span class="sxs-lookup"><span data-stu-id="6c0b3-117">**adSchemaDimensions**</span></span>

  - <span data-ttu-id="6c0b3-118">**adschemahierarchies**</span><span class="sxs-lookup"><span data-stu-id="6c0b3-118">**adSchemaHierarchies**</span></span>

  - <span data-ttu-id="6c0b3-119">**adSchemaLevels**</span><span class="sxs-lookup"><span data-stu-id="6c0b3-119">**adSchemaLevels**</span></span>

  - <span data-ttu-id="6c0b3-120">**adschemameasures**</span><span class="sxs-lookup"><span data-stu-id="6c0b3-120">**adSchemaMeasures**</span></span>

  - <span data-ttu-id="6c0b3-121">**adSchemaMembers**</span><span class="sxs-lookup"><span data-stu-id="6c0b3-121">**adSchemaMembers**</span></span>

<span data-ttu-id="6c0b3-p105">ADO の列挙値を ADO MD のプロパティまたはメソッドで使用するには、プロジェクトで ADO ライブラリと ADO MD ライブラリの両方に対する参照を設定する必要があります。たとえば、ADO の **adState** 列挙値を ADO MD の [State](state-property-ado-md.md) プロパティで使用できます。ライブラリへの参照を確立する方法の詳細については、開発ツールのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-p105">To use ADO enum values with ADO MD properties or methods, your project must reference both the ADO and ADO MD libraries. For example, you can use the ADO **adState** enum values with the ADO MD [State](state-property-ado-md.md) property. For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="6c0b3-125">ADO のオブジェクトおよびメソッドの詳細については、「[ADO API リファレンス](ado-api-reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c0b3-125">For more information about the ADO objects and methods, see the [ADO API Reference](ado-api-reference.md).</span></span>

