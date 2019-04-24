---
title: DataSource プロパティ (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0dec30715d1eb4e31d7490db4cedd015ecf3c040
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294471"
---
# <a name="datasource-property-ado"></a><span data-ttu-id="4a5dd-102">DataSource プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="4a5dd-102">DataSource property (ADO)</span></span>


<span data-ttu-id="4a5dd-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a5dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a5dd-104">[Recordset](recordset-object-ado.md) オブジェクトとして表されるデータを持つオブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-104">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a5dd-105">注釈</span><span class="sxs-lookup"><span data-stu-id="4a5dd-105">Remarks</span></span>

<span data-ttu-id="4a5dd-106">This property is used to create data-bound controls with the Data Environment.</span><span class="sxs-lookup"><span data-stu-id="4a5dd-106">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="4a5dd-107">データ環境には、 **Recordset**オブジェクトとして表される名前付きオブジェクト (*データメンバー*) を含むデータのコレクション (データソース) が保持されて*います。*</span><span class="sxs-lookup"><span data-stu-id="4a5dd-107">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="4a5dd-108">[DataMember](datamember-property-ado.md) プロパティと **DataSource** プロパティは組み合わせて使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-108">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="4a5dd-109">参照されるオブジェクトには、 **IDataSource** インターフェイスを実装し、 **IRowset** インターフェイスを組み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a5dd-109">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="4a5dd-110">**使用例**</span><span class="sxs-lookup"><span data-stu-id="4a5dd-110">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
