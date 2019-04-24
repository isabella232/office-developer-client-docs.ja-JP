---
title: SendEmail マクロ アクション
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314652"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="d8f67-102">SendEmail マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="d8f67-102">SendEmail macro action</span></span>

<span data-ttu-id="d8f67-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8f67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8f67-104">**SendEmail**アクションは、電子メールメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="d8f67-104">The **SendEmail** action sends an email message.</span></span>

> [!NOTE]
> <span data-ttu-id="d8f67-105">**SendEmail** アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d8f67-105">The **SendEmail** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="d8f67-106">Setting</span><span class="sxs-lookup"><span data-stu-id="d8f67-106">Setting</span></span>

<span data-ttu-id="d8f67-107">**SendEmail** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d8f67-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8f67-108">引数</span><span class="sxs-lookup"><span data-stu-id="d8f67-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="d8f67-109">必須</span><span class="sxs-lookup"><span data-stu-id="d8f67-109">Required</span></span></p></th>
<th><p><span data-ttu-id="d8f67-110">説明</span><span class="sxs-lookup"><span data-stu-id="d8f67-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8f67-111"><strong>To/宛先</strong></span><span class="sxs-lookup"><span data-stu-id="d8f67-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="d8f67-112">はい</span><span class="sxs-lookup"><span data-stu-id="d8f67-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="d8f67-113">メッセージで [<strong>宛先</strong>] 行に含めるメッセージ受信者名。この引数 (および <em>Cc</em> 引数と <em>Bcc</em> 引数) で複数の受信者名を指定する場合は、セミコロン (;) で区切ります。</span><span class="sxs-lookup"><span data-stu-id="d8f67-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8f67-114"><strong>Cc/CC</strong></span><span class="sxs-lookup"><span data-stu-id="d8f67-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="d8f67-115">いいえ</span><span class="sxs-lookup"><span data-stu-id="d8f67-115">No</span></span></p></td>
<td><p><span data-ttu-id="d8f67-116">メッセージの Cc (&quot;カーボンコピー&quot;) 行に配置するメッセージの受信者名。</span><span class="sxs-lookup"><span data-stu-id="d8f67-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8f67-117"><strong>Bcc/BCC</strong></span><span class="sxs-lookup"><span data-stu-id="d8f67-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="d8f67-118">いいえ</span><span class="sxs-lookup"><span data-stu-id="d8f67-118">No</span></span></p></td>
<td><p><span data-ttu-id="d8f67-119">メッセージの Bcc (&quot;ブラインドカーボンコピー&quot;) 行に配置するメッセージの受信者名を指定します。</span><span class="sxs-lookup"><span data-stu-id="d8f67-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8f67-120"><strong>Subject/件名</strong></span><span class="sxs-lookup"><span data-stu-id="d8f67-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="d8f67-121">いいえ</span><span class="sxs-lookup"><span data-stu-id="d8f67-121">No</span></span></p></td>
<td><p><span data-ttu-id="d8f67-p101">メッセージの件名。このテキストはメール メッセージの [ <strong>件名</strong> ] 行に表示されます。  </span><span class="sxs-lookup"><span data-stu-id="d8f67-p101">The subject of the message. This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8f67-124"><strong>Body/本文</strong></span><span class="sxs-lookup"><span data-stu-id="d8f67-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="d8f67-125">いいえ</span><span class="sxs-lookup"><span data-stu-id="d8f67-125">No</span></span></p></td>
<td><p><span data-ttu-id="d8f67-p102">メール メッセージの本文に含めるテキスト。この引数を指定しない場合、メッセージにテキストが追加されません。</span><span class="sxs-lookup"><span data-stu-id="d8f67-p102">The text that you want to include in the main body of the mail message. If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d8f67-128">注釈</span><span class="sxs-lookup"><span data-stu-id="d8f67-128">Remarks</span></span>

<span data-ttu-id="d8f67-129">**SendEmail** アクションは、 **[After Delete](after-delete-macro-event.md)** マクロ イベント、 **[After Insert](after-insert-macro-event.md)** マクロ イベント、および **[After Update](after-update-macro-event.md)** マクロ イベントでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d8f67-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="d8f67-130">**SendEmail** アクションでは、メッセージを表示し、編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="d8f67-130">The **SendEmail** action does not display the message for editing.</span></span>

