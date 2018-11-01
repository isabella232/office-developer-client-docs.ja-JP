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
# <a name="save-method-ado"></a><span data-ttu-id="a2aae-102">Save メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="a2aae-102">Save Method (ADO)</span></span>


<span data-ttu-id="a2aae-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a2aae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2aae-104">[Recordset](recordset-object-ado.md) をファイルまたは [Stream](stream-object-ado.md) オブジェクトに保存します。</span><span class="sxs-lookup"><span data-stu-id="a2aae-104">Saves the [Recordset](recordset-object-ado.md) in a file or [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2aae-105">構文</span><span class="sxs-lookup"><span data-stu-id="a2aae-105">Syntax</span></span>

<span data-ttu-id="a2aae-106">*レコード セット*です。*宛先*、 *PersistFormat*を保存します。</span><span class="sxs-lookup"><span data-stu-id="a2aae-106">*recordset*.Save*Destination*, *PersistFormat*</span></span>

## <a name="parameters"></a><span data-ttu-id="a2aae-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a2aae-107">Parameters</span></span>

  - <span data-ttu-id="a2aae-108">*Destination*</span><span class="sxs-lookup"><span data-stu-id="a2aae-108">*Destination*</span></span>

  - <span data-ttu-id="a2aae-p101">省略可能です。 **Recordset** の保存先であるファイルの完全なパス名を表すバリアント型 ( **Variant** ) の値、または **Stream** オブジェクトへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p101">Optional. A **Variant** that represents the complete path name of the file where the **Recordset** is to be saved, or a reference to a **Stream** object.</span></span>

  - <span data-ttu-id="a2aae-111">*PersistFormat*</span><span class="sxs-lookup"><span data-stu-id="a2aae-111">*PersistFormat*</span></span>

  - <span data-ttu-id="a2aae-p102">省略可能です。 [Recordset](persistformatenum.md) の保存形式 (XML または ADTG) を **PersistFormatEnum** 値で指定します。既定値は **adPersistADTG** です。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p102">Optional. A [PersistFormatEnum](persistformatenum.md) value that specifies the format in which the **Recordset** is to be saved (XML or ADTG). The default value is **adPersistADTG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2aae-115">解説</span><span class="sxs-lookup"><span data-stu-id="a2aae-115">Remarks</span></span>

<span data-ttu-id="a2aae-p103">**Save** メソッドは、開いている **Recordset** でのみ呼び出すことができます。保存した **Recordset** を *Destination* から復元するには、[Open](open-method-ado-recordset.md) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p103">The **Save** method can only be invoked on an open **Recordset**. Use the [Open](open-method-ado-recordset.md) method to later restore the **Recordset** from *Destination*.</span></span>

<span data-ttu-id="a2aae-p104">[Filter](filter-property-ado.md) プロパティが **Recordset** に対して有効な場合は、フィルターでアクセスできる行のみが保存されます。 **Recordset** が階層の場合は、親 **Recordset** を含めて、現在の子 **Recordset** とその子が保存されます。子 **Recordset** の **Save** メソッドを呼び出すと、子と、そのすべての子は保存されますが、親は保存されません。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p104">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, then only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, then the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.</span></span>

<span data-ttu-id="a2aae-p105">**Recordset** メソッドを初めて保存するとき、*Destination* は指定してもしなくてもかまいません。*Destination* を省略すると、**Recordset** の [Source](source-property-ado-recordset.md) プロパティの値に設定された名前を使用して、新規ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p105">The first time you save the **Recordset**, it is optional to specify *Destination*. If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="a2aae-123">後で**Save**を呼び出した後、最初の保存、または実行時エラーが発生するときは、*コピー先*を省略します。</span><span class="sxs-lookup"><span data-stu-id="a2aae-123">Omit *Destination* when you subsequently call **Save** after the first save, or a run-time error will occur.</span></span> <span data-ttu-id="a2aae-124">新しい*転送先*と**保存**を後で呼び出すと、**レコード セット**が新しい移動先に保存されます。</span><span class="sxs-lookup"><span data-stu-id="a2aae-124">If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination.</span></span> <span data-ttu-id="a2aae-125">ただし、その場合、新しい保存先と元の保存先の両方が開いています。</span><span class="sxs-lookup"><span data-stu-id="a2aae-125">However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="a2aae-p107">**Save** メソッドは、**Recordset** または *Destination* を閉じません。したがって、**Recordset** の操作を続行し、最新の変更を保存することができます。**Recordset** を閉じるまで、*Destination* は開いたままになります。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p107">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes. *Destination* remains open until the **Recordset** is closed.</span></span>

<span data-ttu-id="a2aae-p108">セキュリティ上の理由により、 **Save** メソッドは、Microsoft Internet Explorer で実行されるスクリプトからは、低レベルおよびカスタムのセキュリティ設定の使用時のみ許可されます。セキュリティに関する問題の詳細については、「Microsoft Data Access Technical Articles Overview」 (英語) の「ADO」 (英語) の、「ADO and RDS Security Issues in Microsoft Internet Explorer」 (英語) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p108">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="a2aae-130">非同期の **Recordset** のフェッチ、実行、または更新の操作中に **Save** メソッドが呼び出された場合、 **Save** メソッドは、非同期操作が完了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="a2aae-130">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, then **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="a2aae-p109">レコードは、 **Recordset** の最初の行から順に保存されます。 **Save** メソッドが終了すると、カレント行の位置は **Recordset** の最初の行になります。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p109">Records are saved beginning with the first row of the **Recordset**. When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="a2aae-p110">最良の結果を得るには、 [Save](cursorlocation-property-ado.md) メソッドの実行時に **CursorLocation** プロパティを **adUseClient** に設定します。 **Recordset** オブジェクトを保存するために必要なすべての機能が、ご使用のプロバイダーによってサポートされていない場合は、Cursor Service によりその機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p110">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**. If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="a2aae-p111">**Recordset** の **CursorLocation** プロパティが **adUseServer** に設定されたままの場合、その **Recordset** の更新機能が制限されます。プロバイダーの機能によって異なりますが、通常は、単一テーブルの更新、挿入、および削除のみが許可されます。この設定では、 [Resync](resync-method-ado.md) メソッドも利用できません。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p111">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited. Typically, only single-table updates, insertions, and deletions are allowed (dependant upon provider functionality). The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a2aae-138">[!メモ] ADO では、 <STRONG>Fields</STRONG> の種類が <STRONG>adVariant</STRONG> 、 <STRONG>adIDispatch</STRONG> 、または <STRONG>adIUnknown</STRONG> に設定された <STRONG>Recordset</STRONG> の保存はサポートされていないため、予期しない結果が生じることがあります。</span><span class="sxs-lookup"><span data-stu-id="a2aae-138">Saving a <STRONG>Recordset</STRONG> with <STRONG>Fields</STRONG> of type <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG>, or <STRONG>adIUnknown</STRONG> is not supported by ADO and can cause unpredictable results.</span></span></P>



<span data-ttu-id="a2aae-139">**フィルター**の抽出条件の文字列形式でのみ (例:"受注日" \> ' 12/31/1999 ') 保存された**レコード セット**の内容に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="a2aae-139">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="a2aae-140">**Bookmarks** の配列で作成されたフィルター、または **FilterGroupEnum** の値を使用して作成されたフィルターは、永続化された **Recordset** の内容に影響しません。</span><span class="sxs-lookup"><span data-stu-id="a2aae-140">Filters created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted **Recordset**.</span></span> <span data-ttu-id="a2aae-141">これらの規則は、クライアント側カーソルまたはサーバー側カーソルを使用して作成された **Recordsets** に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="a2aae-141">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

<span data-ttu-id="a2aae-142">*Destination*パラメーターには、OLE DB IStream インターフェイスをサポートする任意のオブジェクトを使用できますが、あるために、ASP Response オブジェクトに直接**レコード セット**を保存できます。</span><span class="sxs-lookup"><span data-stu-id="a2aae-142">Because the *Destination* parameter can accept any object that supports the OLE DB IStream interface, you can save a **Recordset** directly to the ASP Response object.</span></span> <span data-ttu-id="a2aae-143">詳細については、「 [XML レコードセットを保存するシナリオ](xml-recordset-persistence-scenario.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2aae-143">For more details, please see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

<span data-ttu-id="a2aae-144">次の Visual Basic コードに示すように、XML 形式の **Recordset** を MSXML DOM オブジェクトのインスタンスに保存することもできます。</span><span class="sxs-lookup"><span data-stu-id="a2aae-144">You can also save a **Recordset** in XML format to an instance of an MSXML DOM object, as is shown in the following Visual Basic code:</span></span>


> [!NOTE]
> <P><span data-ttu-id="a2aae-p114">[!メモ] 階層 <STRONG>Recordset</STRONG> (データ シェイプ) を XML 形式で保存するときは、2 つの制限事項があります。階層 <STRONG>Recordset</STRONG> に保留中の更新が含まれている場合は、XML で保存できません。また、パラメーター化された階層 <STRONG>Recordset</STRONG> を保存することはできません。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p114">Two limitations apply when saving hierarchical <STRONG>Recordsets</STRONG> (data shapes) in XML format. You cannot save into XML if the hierarchical <STRONG>Recordset</STRONG> contains pending updates, and you cannot save a parameterized hierarchical <STRONG>Recordset</STRONG>.</span></span></P>



<span data-ttu-id="a2aae-p115">XML 形式で保存した Recordset は、UTF-8 形式を使用して保存されます。このようなファイルを ADO Stream に読み込むと、Stream オブジェクトはストリームの Charset プロパティが UTF-8 形式用の適切な値に設定されていない限り、ストリームから Recordset を開こうとしません。</span><span class="sxs-lookup"><span data-stu-id="a2aae-p115">A Recordset saved in XML format is saved using UTF-8 format. When such a file is loaded into an ADO Stream, the Stream object will not attempt to open a Recordset from the stream unless the Charset property of the stream is set to the appropriate value for UTF-8 format.</span></span>

