---
title: WillConnect イベント (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4148baa827b42f34d9b4d15f2f94df2667959b0c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928314"
---
# <a name="willconnect-event-ado"></a><span data-ttu-id="19e71-102">WillConnect イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="19e71-102">WillConnect event (ADO)</span></span>


<span data-ttu-id="19e71-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="19e71-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="19e71-104">**WillConnect** イベントは、接続が開始される前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="19e71-104">The **WillConnect** event is called before a connection starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e71-105">構文</span><span class="sxs-lookup"><span data-stu-id="19e71-105">Syntax</span></span>

<span data-ttu-id="19e71-106">WillConnect*接続文字列*、*ユーザー Id*、*パスワード*、*オプション*、 *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="19e71-106">WillConnect*ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="19e71-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="19e71-107">Parameters</span></span>

  - <span data-ttu-id="19e71-108">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="19e71-108">*ConnectionString*</span></span>

  - <span data-ttu-id="19e71-109">保留中の接続の接続情報が格納された文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="19e71-109">A **String** that contains connection information for the pending connection.</span></span>

  - <span data-ttu-id="19e71-110">*ユーザー Id*</span><span class="sxs-lookup"><span data-stu-id="19e71-110">*UserID*</span></span>

  - <span data-ttu-id="19e71-111">保留中の接続のユーザー名が格納された文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="19e71-111">A **String** that contains a user name for the pending connection.</span></span>

  - <span data-ttu-id="19e71-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="19e71-112">*Password*</span></span>

  - <span data-ttu-id="19e71-113">保留中の接続のパスワードが格納された文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="19e71-113">A **String** that contains a password for the pending connection.</span></span>

  - <span data-ttu-id="19e71-114">*Options*</span><span class="sxs-lookup"><span data-stu-id="19e71-114">*Options*</span></span>

  - <span data-ttu-id="19e71-p101">プロバイダーが *ConnectionString* を評価する方法を示す長整数型 (**Long**) の値です。オプションは **adAsyncOpen** のみ指定できます。</span><span class="sxs-lookup"><span data-stu-id="19e71-p101">A **Long** value that indicates how the provider should evaluate the *ConnectionString*. Your only option is **adAsyncOpen**.</span></span>

  - <span data-ttu-id="19e71-117">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="19e71-117">*adStatus*</span></span>

  - [<span data-ttu-id="19e71-118">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="19e71-118">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="19e71-p102">このイベントが呼び出されたとき、既定では、このパラメーターは **adStatusOK** に設定されます。保留中の操作の取り消しをイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="19e71-p102">When this event is called, this parameter is set to **adStatusOK** by default. It is set to **adStatusCantDeny** if the event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="19e71-p103">このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。この通知の取り消しを実行する接続操作を要求するには、このパラメーターを **adStatusCancel** に設定します。</span><span class="sxs-lookup"><span data-stu-id="19e71-p103">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. Set this parameter to **adStatusCancel** to request the connection operation that caused cancellation of this notification.</span></span>

  - <span data-ttu-id="19e71-123">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="19e71-123">*pConnection*</span></span>

  - <span data-ttu-id="19e71-p104">このイベント通知が適用される [Connection](connection-object-ado.md) オブジェクト。 **WillConnect** イベント ハンドラーで **Connection** のパラメーターが変更されても、 **Connection** には影響はありません。</span><span class="sxs-lookup"><span data-stu-id="19e71-p104">The [Connection](connection-object-ado.md) object for which this event notification applies. Changes to the parameters of the **Connection** by the **WillConnect** event handler will have no effect on the **Connection**.</span></span>

## <a name="remarks"></a><span data-ttu-id="19e71-126">解説</span><span class="sxs-lookup"><span data-stu-id="19e71-126">Remarks</span></span>

<span data-ttu-id="19e71-p105">**WillConnect** を呼び出したとき、*ConnectionString*、*UserID*、*Password*、および *Options* の各パラメーターの値は、このイベント (保留中の接続) を発生させた操作によって設定され、イベントから制御が戻る前に変更できます。**WillConnect** では、保留中の接続を取り消す要求を返す場合もあります。</span><span class="sxs-lookup"><span data-stu-id="19e71-p105">When **WillConnect** is called, the *ConnectionString*, *UserID*, *Password*, and *Options* parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns. **WillConnect** may return a request that the pending connection be canceled.</span></span>

<span data-ttu-id="19e71-129">このイベントがキャンセルされると、 **ConnectComplete**が**adStatusErrorsOccurred**に設定、 *adStatus*パラメーターで呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="19e71-129">When this event is canceled, **ConnectComplete** will be called with its *adStatus* parameter set to **adStatusErrorsOccurred**.</span></span>

