---
title: ExecuteComplete イベント (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a094968e70ace5e6cba1df184bf0ba57c2d7789
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698093"
---
# <a name="executecomplete-event-ado"></a><span data-ttu-id="52825-102">ExecuteComplete イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="52825-102">ExecuteComplete event (ADO)</span></span>

<span data-ttu-id="52825-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="52825-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52825-104">**ExecuteComplete** イベントは、コマンドが実行を終了した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="52825-104">The **ExecuteComplete** event is called after a command has finished executing.</span></span>

## <a name="syntax"></a><span data-ttu-id="52825-105">構文</span><span class="sxs-lookup"><span data-stu-id="52825-105">Syntax</span></span>

<span data-ttu-id="52825-106">ExecuteComplete*RecordsAffected*、 *pError*、 *adStatus*、 *pCommand*、 *pRecordset*、 *pConnection*</span><span class="sxs-lookup"><span data-stu-id="52825-106">ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="52825-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="52825-107">Parameters</span></span>

|<span data-ttu-id="52825-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="52825-108">Parameter</span></span>|<span data-ttu-id="52825-109">説明</span><span class="sxs-lookup"><span data-stu-id="52825-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="52825-110">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="52825-110">*RecordsAffected*</span></span> |<span data-ttu-id="52825-111">コマンドによって影響を受けるレコードの数を表す長整数型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="52825-111">A **Long** value indicating the number of records affected by the command.</span></span>|
|<span data-ttu-id="52825-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="52825-112">*pError*</span></span> |<span data-ttu-id="52825-p101">[Error](error-object-ado.md) オブジェクトです。 **adStatus** の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="52825-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="52825-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="52825-115">*adStatus*</span></span> |<span data-ttu-id="52825-116">[EventStatusEnum](eventstatusenum.md)。</span><span class="sxs-lookup"><span data-stu-id="52825-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="52825-117">このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="52825-117">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="52825-118">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="52825-118">*pCommand*</span></span> |<span data-ttu-id="52825-p103">実行された [Command](command-object-ado.md) オブジェクトです。明示的に **Command** を作成せずに **Connection.Execute** または **Recordset.Open** を呼び出しても **Command** オブジェクトが格納されます (この場合、 **Command** オブジェクトは ADO によって内部的に作成されます)。</span><span class="sxs-lookup"><span data-stu-id="52825-p103">The [Command](command-object-ado.md) object that was executed. Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.</span></span>|
|<span data-ttu-id="52825-121">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="52825-121">*pRecordset*</span></span> |<span data-ttu-id="52825-p104">実行されたコマンドの結果の [Recordset](recordset-object-ado.md) オブジェクトです。この **Recordset** は空の場合もあります。この Recordset オブジェクトは、このイベント ハンドラーから破棄しないでください。破棄した場合には、ADO が存在しないオブジェクトにアクセスしようとしたときにアクセス違反が発生します。</span><span class="sxs-lookup"><span data-stu-id="52825-p104">A [Recordset](recordset-object-ado.md) object that is the result of the executed command. This **Recordset** may be empty. You should never destroy this Recordset object from within this event handler. Doing so will result in an Access Violation when ADO tries to access an object that no longer exists.</span></span>|
|<span data-ttu-id="52825-126">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="52825-126">*pConnection*</span></span> |<span data-ttu-id="52825-p105">[Connection](connection-object-ado.md) オブジェクトです。操作を実行したときの接続です。</span><span class="sxs-lookup"><span data-stu-id="52825-p105">A [Connection](connection-object-ado.md) object. The connection over which the operation was executed.</span></span>|

## <a name="remarks"></a><span data-ttu-id="52825-129">解説</span><span class="sxs-lookup"><span data-stu-id="52825-129">Remarks</span></span>

<span data-ttu-id="52825-130">**ExecuteComplete** イベントは、 **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)、 **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)、 **Recordset.**[Open](open-method-ado-recordset.md)、 **Recordset.**[Requery](requery-method-ado.md)、または **Recordset.**[NextRecordset](nextrecordset-method-ado.md) の各メソッドにより発生します。</span><span class="sxs-lookup"><span data-stu-id="52825-130">An **ExecuteComplete** event may occur due to the **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md), or **Recordset.**[NextRecordset](nextrecordset-method-ado.md) methods.</span></span>

