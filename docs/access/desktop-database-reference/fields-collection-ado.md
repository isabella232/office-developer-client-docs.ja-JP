---
title: Fields コレクション (ADO)
TOCTitle: Fields Collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9d4b710c8e0a9293c9164395cf9bff3078a3b36
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879404"
---
# <a name="fields-collection-ado"></a>Fields コレクション (ADO)


**適用されます**Access 2013、Office 2013。

[Recordset](field-object-ado.md) オブジェクトまたは [Record](recordset-object-ado.md) オブジェクトのすべての [Field](record-object-ado.md) オブジェクトを格納します。

## <a name="remarks"></a>備考

**Recordset** オブジェクトには、 **Field** オブジェクトから構成される **Fields** コレクションがあります。各 **Field** オブジェクトは、 **Recordset** の 1 つの列に対応します。コレクションの **Refresh** メソッドを呼び出すと、 **Recordset** を開く前に [Fields](refresh-method-ado.md) コレクションにフィールドを追加できます。


> [!NOTE]
> <P>[!メモ] <STRONG>Field</STRONG> オブジェクトの使用方法の詳細については、 <STRONG>Field</STRONG> オブジェクトのトピックを参照してください。</P>



**Fields** コレクションには、条件付きで [Field](append-method-ado.md) オブジェクトを作成しコレクションに追加する **Append** メソッド、および追加や削除を完了させる **Update** メソッドがあります。

**Record** オブジェクトには、 [FieldEnum](fieldenum.md) 定数でインデックスを設定できる 2 つの特別なフィールドがあります。1 つの定数は、 **Record** の既定のストリームを格納するフィールドにアクセスし、もう 1 つの定数は、 **Record** の絶対 URL 文字列を格納するフィールドにアクセスします。

特定のプロバイダー (たとえば、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) は、 **Fields** コレクションに **Record** または **Recordset** の使用可能なフィールドのサブセットを追加できます。他のフィールドは、最初に名前で参照するか、コードでインデックス設定しない限り、コレクションに追加されません。

存在しないフィールドを名前で参照しようとすると、新しい **Field** オブジェクトが **Fields** コレクションに [Status](status-property-ado-field.md) が **adFieldPendingInsert** の状態で追加されます。 [Update](update-method-ado.md) を呼び出すと、プロバイダーで許容される限り、ADO によってデータ ソースに新しいフィールドが作成されます。

