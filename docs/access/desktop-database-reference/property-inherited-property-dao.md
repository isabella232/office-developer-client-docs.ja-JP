---
title: Property.Inherited プロパティ (DAO)
TOCTitle: Inherited Property
ms:assetid: 10e624db-2301-b9be-beca-6e8caccf7274
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845349(v=office.15)
ms:contentKeyID: 48543304
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052991
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7768ec3048c14962154fa8ba54f391a9a8a10e66
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887979"
---
# <a name="propertyinherited-property-dao"></a>Property.Inherited プロパティ (DAO)


**適用されます**Access 2013、Office 2013。 

基になるオブジェクトから **[Property](property-object-dao.md)** オブジェクトが継承されるかどうかを示す値を取得します。

## <a name="syntax"></a>構文

*式*です。継承

*式***Property**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

定義済みのプロパティを表す組み込みの **Property** オブジェクトの場合、可能な戻り値は **False** のみです。

**Inherited** プロパティを使用すると、対象のオブジェクトに対してユーザー定義の **Property** オブジェクトが作成されたかどうか、または別のオブジェクトから **Property** オブジェクトが継承されたかどうかを調べることができます。たとえば、 [**QueryDef**](querydef-object-dao.md) オブジェクトに対して新しい **Property** オブジェクトを作成し、 [QueryDef](recordset-object-dao.md) オブジェクトから ****Recordset**** オブジェクトを開くとします。この新しい **Property** オブジェクトは **Recordset** オブジェクトの **[Properties](properties-collection-dao.md)** コレクションの一部となりますが、Property オブジェクトは **Recordset** オブジェクトではなく **QueryDef** オブジェクトに対して作成されたため、 **Inherited** プロパティは **True** に設定されます。

## <a name="example"></a>例

この例では、 **Inherited** プロパティを使用して、ユーザー定義の **Property** オブジェクトが、 **Recordset** オブジェクトに対して作成されたか、または別の基となるオブジェクトに対して作成されたかを調べます。

```vb 
Sub InheritedX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfTest As TableDef 
 Dim rstTest As Recordset 
 Dim prpNew As Property 
 Dim prpLoop As Property 
 
 ' Create a new property for a saved TableDef object, then 
 ' open a recordset from that TableDef object. 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set tdfTest = dbsNorthwind.TableDefs(0) 
 Set prpNew = tdfTest.CreateProperty("NewProperty", _ 
 dbBoolean, True) 
 tdfTest.Properties.Append prpNew 
 Set rstTest = tdfTest.OpenRecordset(dbOpenForwardOnly) 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the TableDef. 
 Debug.Print "NewProperty of " & tdfTest.Name & _ 
 " TableDef:" 
 Debug.Print " Inherited = " & _ 
 tdfTest.Properties("NewProperty").Inherited 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the Recordset. 
 Debug.Print "NewProperty of " & rstTest.Name & _ 
 " Recordset:" 
 Debug.Print " Inherited = " & _ 
 rstTest.Properties("NewProperty").Inherited 
 
 ' Delete new TableDef because this is a demonstration. 
 tdfTest.Properties.Delete prpNew.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

