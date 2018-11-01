---
title: メソッドを ActiveX データ オブジェクト (ADO) の保存します。
TOCTitle: Save Method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b4e3698043c109a8f0fbf32c5c2b8c8ae20e824
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875982"
---
# <a name="save-method-ado"></a>Save メソッド (ADO)


**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) をファイルまたは [Stream](stream-object-ado.md) オブジェクトに保存します。

## <a name="syntax"></a>構文

*レコード セット*です。*宛先*、 *PersistFormat*を保存します。

## <a name="parameters"></a>パラメーター

  - *Destination*

  - 省略可能です。 **Recordset** の保存先であるファイルの完全なパス名を表すバリアント型 ( **Variant** ) の値、または **Stream** オブジェクトへの参照を指定します。

  - *PersistFormat*

  - 省略可能です。 [Recordset](persistformatenum.md) の保存形式 (XML または ADTG) を **PersistFormatEnum** 値で指定します。既定値は **adPersistADTG** です。

## <a name="remarks"></a>解説

**Save** メソッドは、開いている **Recordset** でのみ呼び出すことができます。保存した **Recordset** を *Destination* から復元するには、[Open](open-method-ado-recordset.md) メソッドを使用します。

[Filter](filter-property-ado.md) プロパティが **Recordset** に対して有効な場合は、フィルターでアクセスできる行のみが保存されます。 **Recordset** が階層の場合は、親 **Recordset** を含めて、現在の子 **Recordset** とその子が保存されます。子 **Recordset** の **Save** メソッドを呼び出すと、子と、そのすべての子は保存されますが、親は保存されません。

**Recordset** メソッドを初めて保存するとき、*Destination* は指定してもしなくてもかまいません。*Destination* を省略すると、**Recordset** の [Source](source-property-ado-recordset.md) プロパティの値に設定された名前を使用して、新規ファイルが作成されます。

後で**Save**を呼び出した後、最初の保存、または実行時エラーが発生するときは、*コピー先*を省略します。 新しい*転送先*と**保存**を後で呼び出すと、**レコード セット**が新しい移動先に保存されます。 ただし、その場合、新しい保存先と元の保存先の両方が開いています。

**Save** メソッドは、**Recordset** または *Destination* を閉じません。したがって、**Recordset** の操作を続行し、最新の変更を保存することができます。**Recordset** を閉じるまで、*Destination* は開いたままになります。

セキュリティ上の理由により、 **Save** メソッドは、Microsoft Internet Explorer で実行されるスクリプトからは、低レベルおよびカスタムのセキュリティ設定の使用時のみ許可されます。セキュリティに関する問題の詳細については、「Microsoft Data Access Technical Articles Overview」 (英語) の「ADO」 (英語) の、「ADO and RDS Security Issues in Microsoft Internet Explorer」 (英語) を参照してください。

非同期の **Recordset** のフェッチ、実行、または更新の操作中に **Save** メソッドが呼び出された場合、 **Save** メソッドは、非同期操作が完了するまで待機します。

レコードは、 **Recordset** の最初の行から順に保存されます。 **Save** メソッドが終了すると、カレント行の位置は **Recordset** の最初の行になります。

最良の結果を得るには、 [Save](cursorlocation-property-ado.md) メソッドの実行時に **CursorLocation** プロパティを **adUseClient** に設定します。 **Recordset** オブジェクトを保存するために必要なすべての機能が、ご使用のプロバイダーによってサポートされていない場合は、Cursor Service によりその機能が提供されます。

**Recordset** の **CursorLocation** プロパティが **adUseServer** に設定されたままの場合、その **Recordset** の更新機能が制限されます。プロバイダーの機能によって異なりますが、通常は、単一テーブルの更新、挿入、および削除のみが許可されます。この設定では、 [Resync](resync-method-ado.md) メソッドも利用できません。


> [!NOTE]
> <P>[!メモ] ADO では、 <STRONG>Fields</STRONG> の種類が <STRONG>adVariant</STRONG> 、 <STRONG>adIDispatch</STRONG> 、または <STRONG>adIUnknown</STRONG> に設定された <STRONG>Recordset</STRONG> の保存はサポートされていないため、予期しない結果が生じることがあります。</P>



**フィルター**の抽出条件の文字列形式でのみ (例:"受注日" \> ' 12/31/1999 ') 保存された**レコード セット**の内容に影響を与えます。 **Bookmarks** の配列で作成されたフィルター、または **FilterGroupEnum** の値を使用して作成されたフィルターは、永続化された **Recordset** の内容に影響しません。 これらの規則は、クライアント側カーソルまたはサーバー側カーソルを使用して作成された **Recordsets** に当てはまります。

*Destination*パラメーターには、OLE DB IStream インターフェイスをサポートする任意のオブジェクトを使用できますが、あるために、ASP Response オブジェクトに直接**レコード セット**を保存できます。 詳細については、「 [XML レコードセットを保存するシナリオ](xml-recordset-persistence-scenario.md)」を参照してください。

次の Visual Basic コードに示すように、XML 形式の **Recordset** を MSXML DOM オブジェクトのインスタンスに保存することもできます。


> [!NOTE]
> <P>[!メモ] 階層 <STRONG>Recordset</STRONG> (データ シェイプ) を XML 形式で保存するときは、2 つの制限事項があります。階層 <STRONG>Recordset</STRONG> に保留中の更新が含まれている場合は、XML で保存できません。また、パラメーター化された階層 <STRONG>Recordset</STRONG> を保存することはできません。</P>



XML 形式で保存した Recordset は、UTF-8 形式を使用して保存されます。このようなファイルを ADO Stream に読み込むと、Stream オブジェクトはストリームの Charset プロパティが UTF-8 形式用の適切な値に設定されていない限り、ストリームから Recordset を開こうとしません。

