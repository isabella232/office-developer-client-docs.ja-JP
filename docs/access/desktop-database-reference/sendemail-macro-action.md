---
title: SendEmail マクロ アクション
TOCTitle: SendEmail Macro Action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db82c2d0c8350d517044df5848f8c264b92e928d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477270"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="161c1-102">SendEmail マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="161c1-102">SendEmail Macro Action</span></span>


<span data-ttu-id="161c1-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="161c1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="161c1-104">**SendEmail** マクロ アクションは、電子メール メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="161c1-104">The **SendEmail** action sends an e-mail message.</span></span>


> [!NOTE]
> <P><span data-ttu-id="161c1-105">[!メモ] <STRONG>SendEmail</STRONG> アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="161c1-105">The <STRONG>SendEmail</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="161c1-106">設定</span><span class="sxs-lookup"><span data-stu-id="161c1-106">Setting</span></span>

<span data-ttu-id="161c1-107">**SendEmail** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="161c1-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="161c1-108">引数</span><span class="sxs-lookup"><span data-stu-id="161c1-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="161c1-109">必須</span><span class="sxs-lookup"><span data-stu-id="161c1-109">Required</span></span></p></th>
<th><p><span data-ttu-id="161c1-110">説明</span><span class="sxs-lookup"><span data-stu-id="161c1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="161c1-111"><strong>To/宛先</strong></span><span class="sxs-lookup"><span data-stu-id="161c1-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="161c1-112">はい</span><span class="sxs-lookup"><span data-stu-id="161c1-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="161c1-113">[メッセージの [<strong>宛先</strong>] 行を追加する名前を持つメッセージの受信者です。セミコロン (;) でこの引数に (および、 <em>Cc</em>と<em>Bcc</em>の引数) を指定した受信者の名前を区切ります。</span><span class="sxs-lookup"><span data-stu-id="161c1-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="161c1-114"><strong>Cc/CC</strong></span><span class="sxs-lookup"><span data-stu-id="161c1-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="161c1-115">いいえ</span><span class="sxs-lookup"><span data-stu-id="161c1-115">No</span></span></p></td>
<td><p><span data-ttu-id="161c1-116">メッセージの受信者、[cc] に入力する名前 (&quot;カーボン コピー&quot;)、メッセージ内の行です。</span><span class="sxs-lookup"><span data-stu-id="161c1-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="161c1-117"><strong>Bcc/BCC</strong></span><span class="sxs-lookup"><span data-stu-id="161c1-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="161c1-118">いいえ</span><span class="sxs-lookup"><span data-stu-id="161c1-118">No</span></span></p></td>
<td><p><span data-ttu-id="161c1-119">メッセージの宛先、Bcc に入力する名前 (&quot;ブラインド カーボン コピー&quot;)、メッセージ内の行です。</span><span class="sxs-lookup"><span data-stu-id="161c1-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="161c1-120"><strong>Subject/件名</strong></span><span class="sxs-lookup"><span data-stu-id="161c1-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="161c1-121">いいえ</span><span class="sxs-lookup"><span data-stu-id="161c1-121">No</span></span></p></td>
<td><p><span data-ttu-id="161c1-p101">メッセージの件名。このテキストはメール メッセージの [ <strong>件名</strong> ] 行に表示されます。  </span><span class="sxs-lookup"><span data-stu-id="161c1-p101">The subject of the message. This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="161c1-124"><strong>Body/本文</strong></span><span class="sxs-lookup"><span data-stu-id="161c1-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="161c1-125">いいえ</span><span class="sxs-lookup"><span data-stu-id="161c1-125">No</span></span></p></td>
<td><p><span data-ttu-id="161c1-p102">メール メッセージの本文に含めるテキスト。この引数を指定しない場合、メッセージにテキストが追加されません。</span><span class="sxs-lookup"><span data-stu-id="161c1-p102">The text that you want to include in the main body of the mail message. If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="161c1-128">解説</span><span class="sxs-lookup"><span data-stu-id="161c1-128">Remarks</span></span>

<span data-ttu-id="161c1-129">**SendEmail** アクションは、 **[After Delete](after-delete-macro-event.md)** マクロ イベント、 **[After Insert](after-insert-macro-event.md)** マクロ イベント、および **[After Update](after-update-macro-event.md)** マクロ イベントでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="161c1-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="161c1-130">**SendEmail** アクションでは、メッセージを表示し、編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="161c1-130">The **SendEmail** action does not display the message for editing.</span></span>

