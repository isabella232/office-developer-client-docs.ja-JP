---
title: Reshape Name プロパティ -- 動的 (ADO)
TOCTitle: Reshape Name Property--Dynamic (ADO)
ms:assetid: 59ef99c8-da40-5cf6-b987-d47ea1433f45
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249307(v=office.15)
ms:contentKeyID: 48545030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f202af564d9e8d3634b895ecf851ddd37e49c4b8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477447"
---
# <a name="reshape-name-property--dynamic-ado"></a>Reshape Name プロパティ -- 動的 (ADO)


**適用されます**Access 2013 |。Office 2013

[Recordset](recordset-object-ado.md) オブジェクトの名前を指定します。

## <a name="return-values"></a>戻り値

**Recordset** の名前である文字列型 ( **String** ) の値を返します。

## <a name="remarks"></a>解説

名前は、接続中、または **Recordset** が閉じられるまで保持されます。

**Reshape Name** プロパティは、主に [Microsoft Data Shaping Service for OLE DB (ADO サービス コンポーネント) ](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)サービス プロバイダーのリシェイプ機能で使用されます。リシェイプでは、一意の名前を使います。

このプロパティは読み取り専用ですが、Recordset の作成時に間接的に設定できます。たとえば、SHAPE コマンド句で Recordset を作成し、それに "AS" キーワードで別名を付けた場合、その別名は Reshape Name プロパティに割り当てられます。別名が宣言されていない場合、Reshape Name プロパティには、データ シェイプ サービスにより生成される一意の名前が割り当てられます。別名が、既存の **Recordset** の名前と同じ場合、それらのいずれかが解放されるまで、いずれの **Recordset** もリシェイプされません。既定の動作は、ADO Connection の "Unique Reshape Names" (「Microsoft Data Shaping Service for OLE DB」を参照) プロパティを TRUE に設定すると変更できます。このように変更すると、名前を一意にする必要のある場合にユーザーによって割り当てられた名前を変更できる権限が、データ シェイプ サービスに与えられます。

**Reshape Name** プロパティは、SHAPE コマンドで **Recordset** を参照する場合や、データ シェイプ サービスで生成したために名前がわからない場合に使用します。その場合、 **Reshape Name** プロパティによって返される文字列にコマンドを連結することによって、SHAPE コマンドを生成できます。

**Reshape Name** は、 **CursorLocation** プロパティを [adUseClient](properties-collection-ado.md) に設定したときに、 [Recordset](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。

