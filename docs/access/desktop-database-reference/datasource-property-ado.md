---
title: DataSource プロパティ (ADO)
TOCTitle: DataSource Property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb1c65adcc6e7c513feeea1a506fc222c6b13e19
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479418"
---
# <a name="datasource-property-ado"></a><span data-ttu-id="be11e-102">DataSource プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="be11e-102">DataSource Property (ADO)</span></span>


<span data-ttu-id="be11e-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="be11e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="be11e-104">[Recordset](recordset-object-ado.md) オブジェクトとして表されるデータを持つオブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="be11e-104">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="be11e-105">解説</span><span class="sxs-lookup"><span data-stu-id="be11e-105">Remarks</span></span>

<span data-ttu-id="be11e-106">データ環境でのデータ バインド コントロールを作成するのにはこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="be11e-106">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="be11e-107">*.* の**Recordset**オブジェクトとして表されるオブジェクト (*データ メンバー*) の名前を格納しているデータ (データ ソース) のコレクションを管理します。</span><span class="sxs-lookup"><span data-stu-id="be11e-107">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="be11e-108">[DataMember](datamember-property-ado.md) プロパティと **DataSource** プロパティは組み合わせて使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be11e-108">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="be11e-109">参照されるオブジェクトには、 **IDataSource** インターフェイスを実装し、 **IRowset** インターフェイスを組み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="be11e-109">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="be11e-110">**使用例**</span><span class="sxs-lookup"><span data-stu-id="be11e-110">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
