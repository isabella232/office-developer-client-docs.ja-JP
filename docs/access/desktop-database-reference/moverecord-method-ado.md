---
title: MoveRecord メソッド (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 022db96a00253793505df6e89603070a6d429a8d
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998869"
---
# <a name="moverecord-method-ado"></a>MoveRecord メソッド (ADO)

**適用されます**Access 2013、Office 2013。
 
[Record](record-object-ado.md) で表されるエンティティを別の場所に移動します。

## <a name="syntax"></a>構文

*レコード*です。関係 (*ソース*、*変換先*、*ユーザー名*、*パスワード*、*オプション*、*非同期*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |省略可能です。移動する **Record** を示す URL を含む文字列型 (**String**) の値を指定します。*Source* を省略するか、または空文字列を指定すると、この **Record** で表されるオブジェクトが移動されます。たとえば、**Record** がファイルを表している場合は、ファイルの内容が *Destination* で指定した場所に移動されます。|
|*Destination* |省略可能です。 *ソース*の移動先の場所を指定する URL を含む**文字列**値。|
|*UserName* |省略可能です。*Destination* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。|
|*Password* |省略可能です。*UserName* を確認するためのパスワードを含む、文字列型 (**String**) を指定します。|
|*Options* |省略可能です。[MoveRecordOptionsEnum](moverecordoptionsenum.md) 値を指定します。既定値は、 **adMoveUnspecified** です。このメソッドの動作を指定します。|
|*Async* |省略可能。 **ブール型**の値**true の場合**、この操作を非同期にする必要がありますを指定します。|

## <a name="return-value"></a>戻り値

文字列型 ( **String** ) の値を返します。 通常、*送信先*の値が返されます。 ただし、実際に返される値はプロバイダーによって異なります。

## <a name="remarks"></a>解説

*送信元*と*送信先*の値いない必要があります同じです。それ以外の場合、実行時エラーが発生します。 少なくともサーバー、パス、およびリソース名は異なる必要があります。

Internet Publishing Provider を使用して移動されるファイルでは、*Options* で特に指定のない限り、移動されるファイル内のすべてのハイパーテキスト リンクが更新されます。*Destination* に既存のオブジェクト (たとえば、ファイルまたはディレクトリ) を指定する場合、**adMoveOverWrite** が指定されていないと、このメソッドは失敗します。

> [!NOTE]
> [!メモ] **adMoveOverWrite** オプションは十分に注意して使用してください。たとえば、ファイルをディレクトリに移動するときにこのオプションを指定していると、移動先のディレクトリが "削除" され、移動元のファイルに置き換えられます。

この操作の終了後、 **Record** オブジェクトの一部の属性 ( [ParentURL](parenturl-property-ado.md) プロパティなど) は更新されなくなります。 **Record** オブジェクトのプロパティを更新するには、 **Record** を閉じ、そのファイルまたはディレクトリが移動された場所の URL でもう一度開いてください。

**Recordset** から取得した [Record](recordset-object-ado.md) の場合、ファイルまたはディレクトリの移動後の場所は、 **Recordset** にすぐには反映されません。反映するには、 **Recordset** をいったん閉じてもう一度開いてください。

> [!NOTE]
> [!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。


