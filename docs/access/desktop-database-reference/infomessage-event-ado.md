---
title: InfoMessage イベント (ADO)
TOCTitle: InfoMessage Event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6cc3b69eb3310d8e717605edd3d6fae32d635806
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479602"
---
# <a name="infomessage-event-ado"></a><span data-ttu-id="2e94e-102">InfoMessage イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="2e94e-102">InfoMessage Event (ADO)</span></span>


<span data-ttu-id="2e94e-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e94e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2e94e-104">**InfoMessage** イベントは、 **ConnectionEvent** 操作時に警告が発生するたびに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e94e-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e94e-105">構文</span><span class="sxs-lookup"><span data-stu-id="2e94e-105">Syntax</span></span>

<span data-ttu-id="2e94e-106">InfoMessage*pError*、 *adStatus*、 *pConnection*</span><span class="sxs-lookup"><span data-stu-id="2e94e-106">InfoMessage*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="2e94e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2e94e-107">Parameters</span></span>

  - <span data-ttu-id="2e94e-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="2e94e-108">*pError*</span></span>

  - <span data-ttu-id="2e94e-p101">[Error](error-object-ado.md) オブジェクトです。このパラメーターには、返されたすべてのエラーが格納されます。複数のエラーが返される場合、 **Errors** コレクションを列挙してエラーを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2e94e-p101">An [Error](error-object-ado.md) object. This parameter contains any errors that are returned. If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>

  - <span data-ttu-id="2e94e-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="2e94e-112">*adStatus*</span></span>

  - [<span data-ttu-id="2e94e-113">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="2e94e-113">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="2e94e-114">このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2e94e-114">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="2e94e-115">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="2e94e-115">*pConnection*</span></span>

  - <span data-ttu-id="2e94e-p102">[Connection](connection-object-ado.md) オブジェクトです。警告が発生した接続です。たとえば、 **Connection** オブジェクトを開いたり、 [Connection](command-object-ado.md) で **Command** コマンドを実行したときに、警告が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2e94e-p102">A [Connection](connection-object-ado.md) object. The connection for which the warning occurred. For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>

