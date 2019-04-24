---
title: DataMember プロパティ (ADO)
TOCTitle: DataMember property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 410f11af8daf3912dca9dc78a1cb9216ff8f8dd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294492"
---
# <a name="datamember-property-ado"></a><span data-ttu-id="8b4c4-102">DataMember プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="8b4c4-102">DataMember property (ADO)</span></span>

<span data-ttu-id="8b4c4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b4c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b4c4-104">[DataSource](datasource-property-ado.md) プロパティによって参照されるオブジェクトから取得するデータ メンバーの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="8b4c4-104">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8b4c4-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="8b4c4-105">Settings and return values</span></span>

<span data-ttu-id="8b4c4-106">**String** の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="8b4c4-106">Sets or returns a **String** value.</span></span> <span data-ttu-id="8b4c4-107">名前の大文字と小文字は区別されません。</span><span class="sxs-lookup"><span data-stu-id="8b4c4-107">The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b4c4-108">注釈</span><span class="sxs-lookup"><span data-stu-id="8b4c4-108">Remarks</span></span>

<span data-ttu-id="8b4c4-109">This property is used to create data-bound controls with the Data Environment.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-109">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="8b4c4-110">データ環境には、 [Recordset](recordset-object-ado.md)オブジェクトとして表される名前付きオブジェクト (*データメンバー*) を含むデータのコレクション (データソース) が保持されて*います。*</span><span class="sxs-lookup"><span data-stu-id="8b4c4-110">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="8b4c4-111">**DataMember** プロパティと **DataSource** プロパティは組み合わせて使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b4c4-111">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="8b4c4-p103">**DataMember** プロパティは、 **DataSource** プロパティに指定されたどのオブジェクトを **Recordset** オブジェクトとして表すかを指定します。 **Recordset** オブジェクトは、このプロパティを設定する前に閉じておく必要があります。 **DataSource** プロパティの前に **DataMember** プロパティが設定されていない場合、または **DataMember** 名が、 **DataSource** プロパティに指定されているオブジェクトに認識されない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="8b4c4-p103">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object. The **Recordset** object must be closed before this property is set. An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="8b4c4-115">**使用例**</span><span class="sxs-lookup"><span data-stu-id="8b4c4-115">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
