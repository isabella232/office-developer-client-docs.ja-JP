---
title: MoveRecord メソッド (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d5c3abebc80dea7d5871faa7926cf81bdd9a681f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606570"
---
# <a name="moverecord-method-ado"></a>MoveRecord メソッド (ADO)

**適用先**: Access 2013、Office 2013
 
[Record](record-object-ado.md) で表されるエンティティを別の場所に移動します。

## <a name="syntax"></a>構文

*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |省略可能です。移動する **Record** を示す URL を含む文字列型 (**String**) の値を指定します。*Source* を省略するか、または空文字列を指定すると、この **Record** で表されるオブジェクトが移動されます。たとえば、**Record** がファイルを表している場合は、ファイルの内容が *Destination* で指定した場所に移動されます。|
|*宛先* |省略可能です。*Source* の移動先の場所を指定する URL を含む文字列型 (**String**) の値を指定します。|
|*UserName* |省略可能です。*Destination* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。|
|*Password* |省略可能です。*UserName* を確認するためのパスワードを含む、文字列型 (**String**) を指定します。|
|*Options* |省略可能です。[MoveRecordOptionsEnum](moverecordoptionsenum.md) 値を指定します。既定値は、 **adMoveUnspecified** です。このメソッドの動作を指定します。|
|*Async* |オプション。 True **の** 場合 **、この操作** を非同期に指定するブール値。|

## <a name="return-value"></a>戻り値

文字列型 (**String**) の値を返します。通常は、*Destination* の値が返されます。ただし、実際に返される値はプロバイダーによって異なります。

## <a name="remarks"></a>注釈

*Source* と *Destination* の値は異なっている必要があります。値が等しい場合、実行時エラーが発生します。サーバー名、パス名、およびリソース名のうち、少なくとも 1 つが異なっている必要があります。

Internet Publishing Provider を使用して移動されるファイルでは、*Options* で特に指定のない限り、移動されるファイル内のすべてのハイパーテキスト リンクが更新されます。*Destination* に既存のオブジェクト (たとえば、ファイルまたはディレクトリ) を指定する場合、**adMoveOverWrite** が指定されていないと、このメソッドは失敗します。

> [!NOTE]
> [!メモ] **adMoveOverWrite** オプションは十分に注意して使用してください。たとえば、ファイルをディレクトリに移動するときにこのオプションを指定していると、移動先のディレクトリが "削除" され、移動元のファイルに置き換えられます。

この操作の終了後、 **Record** オブジェクトの一部の属性 ( [ParentURL](parenturl-property-ado.md) プロパティなど) は更新されなくなります。 **Record** オブジェクトのプロパティを更新するには、 **Record** を閉じ、そのファイルまたはディレクトリが移動された場所の URL でもう一度開いてください。

**Recordset** から取得した [Record](recordset-object-ado.md) の場合、ファイルまたはディレクトリの移動後の場所は、 **Recordset** にすぐには反映されません。反映するには、 **Recordset** をいったん閉じてもう一度開いてください。

> [!NOTE]
> [!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、「絶対 URL と [相対 URL」を参照してください](absolute-and-relative-urls.md)。


