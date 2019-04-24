---
title: Save メソッド-ActiveX データオブジェクト (ADO)
TOCTitle: Save method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0a3762c3d4fdb8cc833259b0435b225690d677ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308919"
---
# <a name="save-method-ado"></a>Save メソッド (ADO)

**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) をファイルまたは [Stream](stream-object-ado.md) オブジェクトに保存します。

## <a name="syntax"></a>構文

*recordset*。保存*先*、 *persistformat*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Destination* |省略可能です。 **Recordset** の保存先であるファイルの完全なパス名を表すバリアント型 ( **Variant** ) の値、または **Stream** オブジェクトへの参照を指定します。|
|*persistformat* |省略可能です。 [Recordset](persistformatenum.md) の保存形式 (XML または ADTG) を **PersistFormatEnum** 値で指定します。既定値は **adPersistADTG** です。|

## <a name="remarks"></a>注釈

**Save** メソッドは、開いている **Recordset** でのみ呼び出すことができます。保存した **Recordset** を *Destination* から復元するには、[Open](open-method-ado-recordset.md) メソッドを使用します。

[Filter](filter-property-ado.md) プロパティが **Recordset** に対して有効な場合は、フィルターでアクセスできる行のみが保存されます。 **Recordset** が階層の場合は、親 **Recordset** を含めて、現在の子 **Recordset** とその子が保存されます。子 **Recordset** の **Save** メソッドを呼び出すと、子と、そのすべての子は保存されますが、親は保存されません。

**Recordset** メソッドを初めて保存するとき、*Destination* は指定してもしなくてもかまいません。*Destination* を省略すると、**Recordset** の [Source](source-property-ado-recordset.md) プロパティの値に設定された名前を使用して、新規ファイルが作成されます。

初めて保存した後に、続けて **Save** を呼び出すときは、*Destination* を指定しないでください。指定すると、実行時エラーが発生します。**Save** メソッドを続けて呼び出すときに新しい *Destination* を指定すると、**Recordset** は新しい保存先に保存されます。ただし、その場合、新しい保存先と元の保存先の両方が開いた状態になります。

**Save** メソッドは、**Recordset** または *Destination* を閉じません。したがって、**Recordset** の操作を続行し、最新の変更を保存することができます。**Recordset** を閉じるまで、*Destination* は開いたままになります。

セキュリティ上の理由により、 **Save** メソッドは、Microsoft Internet Explorer で実行されるスクリプトからは、低レベルおよびカスタムのセキュリティ設定の使用時のみ許可されます。セキュリティに関する問題の詳細については、「Microsoft Data Access Technical Articles Overview」 (英語) の「ADO」 (英語) の、「ADO and RDS Security Issues in Microsoft Internet Explorer」 (英語) を参照してください。

非同期の **Recordset** のフェッチ、実行、または更新の操作中に **Save** メソッドが呼び出された場合、 **Save** メソッドは、非同期操作が完了するまで待機します。

レコードは、 **Recordset** の最初の行から順に保存されます。 **Save** メソッドが終了すると、カレント行の位置は **Recordset** の最初の行になります。

最良の結果を得るには、 [Save](cursorlocation-property-ado.md) メソッドの実行時に **CursorLocation** プロパティを **adUseClient** に設定します。 **Recordset** オブジェクトを保存するために必要なすべての機能が、ご使用のプロバイダーによってサポートされていない場合は、Cursor Service によりその機能が提供されます。

**Recordset** の **CursorLocation** プロパティが **adUseServer** に設定されたままの場合、その **Recordset** の更新機能が制限されます。プロバイダーの機能によって異なりますが、通常は、単一テーブルの更新、挿入、および削除のみが許可されます。この設定では、 [Resync](resync-method-ado.md) メソッドも利用できません。

> [!NOTE]
> [!メモ] ADO では、 **Fields** の種類が **adVariant** 、 **adIDispatch** 、または **adIUnknown** に設定された **Recordset** の保存はサポートされていないため、予期しない結果が生じることがあります。

条件**** 文字列の形式 (たとえば、OrderDate \> ' 12/31/1999 ') のフィルターのみが、永続化された**Recordset**の内容に影響します。 **Bookmarks** の配列で作成されたフィルター、または **FilterGroupEnum** の値を使用して作成されたフィルターは、永続化された **Recordset** の内容に影響しません。 これらの規則は、クライアント側カーソルまたはサーバー側カーソルを使用して作成された **Recordsets** に当てはまります。

*Destination* パラメーターには、OLE DB IStream インターフェイスをサポートするすべてのオブジェクトを指定できるので、**Recordset** を ASP Response オブジェクトに直接保存することができます。詳細については、「[XML レコードセットを保存するシナリオ](xml-recordset-persistence-scenario.md)」を参照してください。

次の Visual Basic コードに示すように、XML 形式の **Recordset** を MSXML DOM オブジェクトのインスタンスに保存することもできます。

> [!NOTE]
> [!メモ] 階層 **Recordset** (データ シェイプ) を XML 形式で保存するときは、2 つの制限事項があります。階層 **Recordset** に保留中の更新が含まれている場合は、XML で保存できません。また、パラメーター化された階層 **Recordset** を保存することはできません。

XML 形式で保存した Recordset は、UTF-8 形式を使用して保存されます。このようなファイルを ADO Stream に読み込むと、Stream オブジェクトはストリームの Charset プロパティが UTF-8 形式用の適切な値に設定されていない限り、ストリームから Recordset を開こうとしません。

