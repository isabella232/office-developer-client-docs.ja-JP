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
# <a name="save-method-ado"></a><span data-ttu-id="81c23-102">Save メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="81c23-102">Save method (ADO)</span></span>

<span data-ttu-id="81c23-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="81c23-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81c23-104">[Recordset](recordset-object-ado.md) をファイルまたは [Stream](stream-object-ado.md) オブジェクトに保存します。</span><span class="sxs-lookup"><span data-stu-id="81c23-104">Saves the [Recordset](recordset-object-ado.md) in a file or [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="81c23-105">構文</span><span class="sxs-lookup"><span data-stu-id="81c23-105">Syntax</span></span>

<span data-ttu-id="81c23-106">*recordset*。保存*先*、 *persistformat*</span><span class="sxs-lookup"><span data-stu-id="81c23-106">*recordset*.Save*Destination*, *PersistFormat*</span></span>

## <a name="parameters"></a><span data-ttu-id="81c23-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81c23-107">Parameters</span></span>

|<span data-ttu-id="81c23-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81c23-108">Parameter</span></span>|<span data-ttu-id="81c23-109">説明</span><span class="sxs-lookup"><span data-stu-id="81c23-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="81c23-110">*Destination*</span><span class="sxs-lookup"><span data-stu-id="81c23-110">*Destination*</span></span> |<span data-ttu-id="81c23-p101">省略可能です。 **Recordset** の保存先であるファイルの完全なパス名を表すバリアント型 ( **Variant** ) の値、または **Stream** オブジェクトへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="81c23-p101">Optional. A **Variant** that represents the complete path name of the file where the **Recordset** is to be saved, or a reference to a **Stream** object.</span></span>|
|<span data-ttu-id="81c23-113">*persistformat*</span><span class="sxs-lookup"><span data-stu-id="81c23-113">*PersistFormat*</span></span> |<span data-ttu-id="81c23-p102">省略可能です。 [Recordset](persistformatenum.md) の保存形式 (XML または ADTG) を **PersistFormatEnum** 値で指定します。既定値は **adPersistADTG** です。</span><span class="sxs-lookup"><span data-stu-id="81c23-p102">Optional. A [PersistFormatEnum](persistformatenum.md) value that specifies the format in which the **Recordset** is to be saved (XML or ADTG). The default value is **adPersistADTG**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="81c23-117">注釈</span><span class="sxs-lookup"><span data-stu-id="81c23-117">Remarks</span></span>

<span data-ttu-id="81c23-p103">**Save** メソッドは、開いている **Recordset** でのみ呼び出すことができます。保存した **Recordset** を *Destination* から復元するには、[Open](open-method-ado-recordset.md) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="81c23-p103">The **Save** method can only be invoked on an open **Recordset**. Use the [Open](open-method-ado-recordset.md) method to later restore the **Recordset** from *Destination*.</span></span>

<span data-ttu-id="81c23-p104">[Filter](filter-property-ado.md) プロパティが **Recordset** に対して有効な場合は、フィルターでアクセスできる行のみが保存されます。 **Recordset** が階層の場合は、親 **Recordset** を含めて、現在の子 **Recordset** とその子が保存されます。子 **Recordset** の **Save** メソッドを呼び出すと、子と、そのすべての子は保存されますが、親は保存されません。</span><span class="sxs-lookup"><span data-stu-id="81c23-p104">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, then only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, then the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.</span></span>

<span data-ttu-id="81c23-p105">**Recordset** メソッドを初めて保存するとき、*Destination* は指定してもしなくてもかまいません。*Destination* を省略すると、**Recordset** の [Source](source-property-ado-recordset.md) プロパティの値に設定された名前を使用して、新規ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="81c23-p105">The first time you save the **Recordset**, it is optional to specify *Destination*. If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="81c23-p106">初めて保存した後に、続けて **Save** を呼び出すときは、*Destination* を指定しないでください。指定すると、実行時エラーが発生します。**Save** メソッドを続けて呼び出すときに新しい *Destination* を指定すると、**Recordset** は新しい保存先に保存されます。ただし、その場合、新しい保存先と元の保存先の両方が開いた状態になります。</span><span class="sxs-lookup"><span data-stu-id="81c23-p106">Omit *Destination* when you subsequently call **Save** after the first save, or a run-time error will occur. If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination. However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="81c23-p107">**Save** メソッドは、**Recordset** または *Destination* を閉じません。したがって、**Recordset** の操作を続行し、最新の変更を保存することができます。**Recordset** を閉じるまで、*Destination* は開いたままになります。</span><span class="sxs-lookup"><span data-stu-id="81c23-p107">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes. *Destination* remains open until the **Recordset** is closed.</span></span>

<span data-ttu-id="81c23-p108">セキュリティ上の理由により、 **Save** メソッドは、Microsoft Internet Explorer で実行されるスクリプトからは、低レベルおよびカスタムのセキュリティ設定の使用時のみ許可されます。セキュリティに関する問題の詳細については、「Microsoft Data Access Technical Articles Overview」 (英語) の「ADO」 (英語) の、「ADO and RDS Security Issues in Microsoft Internet Explorer」 (英語) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81c23-p108">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="81c23-132">非同期の **Recordset** のフェッチ、実行、または更新の操作中に **Save** メソッドが呼び出された場合、 **Save** メソッドは、非同期操作が完了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="81c23-132">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, then **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="81c23-p109">レコードは、 **Recordset** の最初の行から順に保存されます。 **Save** メソッドが終了すると、カレント行の位置は **Recordset** の最初の行になります。</span><span class="sxs-lookup"><span data-stu-id="81c23-p109">Records are saved beginning with the first row of the **Recordset**. When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="81c23-p110">最良の結果を得るには、 [Save](cursorlocation-property-ado.md) メソッドの実行時に **CursorLocation** プロパティを **adUseClient** に設定します。 **Recordset** オブジェクトを保存するために必要なすべての機能が、ご使用のプロバイダーによってサポートされていない場合は、Cursor Service によりその機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="81c23-p110">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**. If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="81c23-p111">**Recordset** の **CursorLocation** プロパティが **adUseServer** に設定されたままの場合、その **Recordset** の更新機能が制限されます。プロバイダーの機能によって異なりますが、通常は、単一テーブルの更新、挿入、および削除のみが許可されます。この設定では、 [Resync](resync-method-ado.md) メソッドも利用できません。</span><span class="sxs-lookup"><span data-stu-id="81c23-p111">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited. Typically, only single-table updates, insertions, and deletions are allowed (dependant upon provider functionality). The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="81c23-140">[!メモ] ADO では、 **Fields** の種類が **adVariant** 、 **adIDispatch** 、または **adIUnknown** に設定された **Recordset** の保存はサポートされていないため、予期しない結果が生じることがあります。</span><span class="sxs-lookup"><span data-stu-id="81c23-140">Saving a **Recordset** with **Fields** of type **adVariant**, **adIDispatch**, or **adIUnknown** is not supported by ADO and can cause unpredictable results.</span></span>

<span data-ttu-id="81c23-141">条件\*\*\*\* 文字列の形式 (たとえば、OrderDate \> ' 12/31/1999 ') のフィルターのみが、永続化された**Recordset**の内容に影響します。</span><span class="sxs-lookup"><span data-stu-id="81c23-141">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="81c23-142">**Bookmarks** の配列で作成されたフィルター、または **FilterGroupEnum** の値を使用して作成されたフィルターは、永続化された **Recordset** の内容に影響しません。</span><span class="sxs-lookup"><span data-stu-id="81c23-142">Filters created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted **Recordset**.</span></span> <span data-ttu-id="81c23-143">これらの規則は、クライアント側カーソルまたはサーバー側カーソルを使用して作成された **Recordsets** に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="81c23-143">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

<span data-ttu-id="81c23-p113">*Destination* パラメーターには、OLE DB IStream インターフェイスをサポートするすべてのオブジェクトを指定できるので、**Recordset** を ASP Response オブジェクトに直接保存することができます。詳細については、「[XML レコードセットを保存するシナリオ](xml-recordset-persistence-scenario.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81c23-p113">Because the *Destination* parameter can accept any object that supports the OLE DB IStream interface, you can save a **Recordset** directly to the ASP Response object. For more details, please see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

<span data-ttu-id="81c23-146">次の Visual Basic コードに示すように、XML 形式の **Recordset** を MSXML DOM オブジェクトのインスタンスに保存することもできます。</span><span class="sxs-lookup"><span data-stu-id="81c23-146">You can also save a **Recordset** in XML format to an instance of an MSXML DOM object, as is shown in the following Visual Basic code:</span></span>

> [!NOTE]
> <span data-ttu-id="81c23-p114">[!メモ] 階層 **Recordset** (データ シェイプ) を XML 形式で保存するときは、2 つの制限事項があります。階層 **Recordset** に保留中の更新が含まれている場合は、XML で保存できません。また、パラメーター化された階層 **Recordset** を保存することはできません。</span><span class="sxs-lookup"><span data-stu-id="81c23-p114">Two limitations apply when saving hierarchical **Recordsets** (data shapes) in XML format. You cannot save into XML if the hierarchical **Recordset** contains pending updates, and you cannot save a parameterized hierarchical **Recordset**.</span></span>

<span data-ttu-id="81c23-p115">XML 形式で保存した Recordset は、UTF-8 形式を使用して保存されます。このようなファイルを ADO Stream に読み込むと、Stream オブジェクトはストリームの Charset プロパティが UTF-8 形式用の適切な値に設定されていない限り、ストリームから Recordset を開こうとしません。</span><span class="sxs-lookup"><span data-stu-id="81c23-p115">A Recordset saved in XML format is saved using UTF-8 format. When such a file is loaded into an ADO Stream, the Stream object will not attempt to open a Recordset from the stream unless the Charset property of the stream is set to the appropriate value for UTF-8 format.</span></span>

