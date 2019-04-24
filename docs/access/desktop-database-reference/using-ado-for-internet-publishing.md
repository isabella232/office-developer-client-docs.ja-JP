---
title: インターネット発行に ADO を使用する
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae8341151c7bf7d90585794061647ba33a5c4ea7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305902"
---
# <a name="using-ado-for-internet-publishing"></a><span data-ttu-id="a382e-102">Internet Publishing 用の ADO の使用</span><span class="sxs-lookup"><span data-stu-id="a382e-102">Using ADO for Internet publishing</span></span>


<span data-ttu-id="a382e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a382e-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="a382e-104">「[OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md)」では、ADO を使用して異種データにアクセスする場合の具体的な例が示されています。</span><span class="sxs-lookup"><span data-stu-id="a382e-104">[The OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) shows a specific example of accessing heterogeneous data with ADO.</span></span> <span data-ttu-id="a382e-105">このセクションの例は、インターネット発行プロバイダーの使用に固有のものですが、他のプロバイダーとの ADO を電子メールストアのプロバイダーなどの異種データに対して使用する場合には、この原則は似ています。</span><span class="sxs-lookup"><span data-stu-id="a382e-105">While the examples in this section will be specific to using the Internet Publishing Provider, the principles demonstrated should be similar when using ADO with other providers to heterogeneous data, such as a provider to an email store.</span></span>

## <a name="urls"></a><span data-ttu-id="a382e-106">URL</span><span class="sxs-lookup"><span data-stu-id="a382e-106">URLs</span></span>

<span data-ttu-id="a382e-p102">接続文字列およびコマンド テキストの代わりに Uniform Resource Locator (URL) を使用して、データ ソースおよびファイルやディレクトリの場所を指定することができます。既存の [Connection](connection-object-ado.md) オブジェクトや **Recordset** オブジェクトだけでなく、 **Record** オブジェクトや **Stream** オブジェクトでも URL を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a382e-p102">Uniform Resource Locators (URLs) can be used as an alternative to connection strings and command text to specify data sources and the location of files and directories. You can use URLs with the existing [Connection](connection-object-ado.md) and **Recordset** objects as well as with the **Record** and **Stream** objects.</span></span>

<span data-ttu-id="a382e-109">URL の使用の詳細については、「[絶対 URL と相対 URL](absolute-and-relative-urls.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a382e-109">For more information about using URLs, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span>

## <a name="record-fields"></a><span data-ttu-id="a382e-110">レコードのフィールド</span><span class="sxs-lookup"><span data-stu-id="a382e-110">Record Fields</span></span>

<span data-ttu-id="a382e-p103">The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or **Record**, can have a different set of columns, or **Fields**. For homogeneous data, each row has the same set of columns. For more information about the fields specific to the Internet Publishing Provider, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="a382e-p103">The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or **Record**, can have a different set of columns, or **Fields**. For homogeneous data, each row has the same set of columns. For more information about the fields specific to the Internet Publishing Provider, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>

## <a name="appending-new-fields"></a><span data-ttu-id="a382e-114">新規フィールドの追加</span><span class="sxs-lookup"><span data-stu-id="a382e-114">Appending New Fields</span></span>

<span data-ttu-id="a382e-115">一部の ADO オブジェクトは、**Record** オブジェクトおよび **Stream** オブジェクトと連携するように拡張されています。</span><span class="sxs-lookup"><span data-stu-id="a382e-115">Several ADO objects have been enhanced to work in conjunction with **Record** and **Stream** objects.</span></span>

  - <span data-ttu-id="a382e-116">[Fields](fields-collection-ado.md) コレクションの [Append](append-method-ado.md) メソッドは、 [Field](field-object-ado.md) オブジェクトを作成してコレクションに追加しますが、 **Field** の値を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="a382e-116">The [Fields](fields-collection-ado.md) collection [Append](append-method-ado.md) method, which creates and adds a [Field](field-object-ado.md) object to the collection, can also specify the value of the **Field**.</span></span>

  - <span data-ttu-id="a382e-117">[Update](update-method-ado.md) メソッドは、フィールドのコレクションへの追加またはコレクションからの削除を終結します。</span><span class="sxs-lookup"><span data-stu-id="a382e-117">The [Update](update-method-ado.md) method finalizes the addition or deletion of fields to the collection.</span></span>

  - <span data-ttu-id="a382e-118">**Append** メソッドに対するショートカットおよび代替手段として、未定義のフィールドまたは以前に削除されたフィールドに値を代入するだけで、フィールドを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="a382e-118">As a shortcut and alternative to the **Append** method, you may create fields by simply assigning a value to an undefined or previously deleted field.</span></span>

## <a name="see-also"></a><span data-ttu-id="a382e-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="a382e-119">See also</span></span>

- [<span data-ttu-id="a382e-120">インターネット発行シナリオのトピック</span><span class="sxs-lookup"><span data-stu-id="a382e-120">Internet Publishing Scenario topics</span></span>](internet-publishing-scenario.md)
