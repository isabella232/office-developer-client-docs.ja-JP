---
title: Bookmark プロパティ (ADO)
TOCTitle: Bookmark property (ADO)
ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15)
ms:contentKeyID: 48543287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 17818fe2b4f826cbcfbbb3955817c2b5d99ab6a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296795"
---
# <a name="bookmark-property-ado"></a><span data-ttu-id="5e146-102">Bookmark プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="5e146-102">Bookmark property (ADO)</span></span>


<span data-ttu-id="5e146-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e146-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5e146-104">[Recordset](recordset-object-ado.md) オブジェクトでカレント レコードを一意に識別するブックマークを示します。または、 **Recordset** オブジェクトのカレント レコードを、有効なブックマークで識別されるレコードに設定します。</span><span class="sxs-lookup"><span data-stu-id="5e146-104">Indicates a bookmark that uniquely identifies the current record in a [Recordset](recordset-object-ado.md) object or sets the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5e146-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="5e146-105">Settings and return values</span></span>

<span data-ttu-id="5e146-106">有効なブックマークとして評価されるバリアント型 (**Variant**) の式を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="5e146-106">Sets or returns a **Variant** expression that evaluates to a valid bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e146-107">注釈</span><span class="sxs-lookup"><span data-stu-id="5e146-107">Remarks</span></span>

<span data-ttu-id="5e146-p101">**Bookmark** プロパティを使用すると、カレント レコードの位置を保存しておき、いつでもそのレコードに戻ることができます。ブックマークは、ブックマーク機能をサポートしている **Recordset** オブジェクトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5e146-p101">Use the **Bookmark** property to save the position of the current record and return to that record at any time. Bookmarks are available only in **Recordset** objects that support bookmark functionality.</span></span>

<span data-ttu-id="5e146-p102">**Recordset** オブジェクトを開くと、各レコードには一意のブックマークが割り当てられます。カレント レコードのブックマークを保存するには、 **Bookmark** プロパティの値を変数に代入します。別のレコードに移動した後、 **Recordset** オブジェクトの **Bookmark** プロパティをその変数の値に設定すると、いつでもそのレコードに戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="5e146-p102">When you open a **Recordset** object, each of its records has a unique bookmark. To save the bookmark for the current record, assign the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="5e146-p103">ユーザーがブックマークの値を見ることはできません。また、ブックマークを直接比較できるとは想定しないでください。同じレコードを参照する 2 つのブックマークであっても、互いに異なる値を持つ場合もあります。</span><span class="sxs-lookup"><span data-stu-id="5e146-p103">The user may not be able to view the value of the bookmark. Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</span></span>

<span data-ttu-id="5e146-p104">[Clone](clone-method-ado.md) メソッドを使用して **Recordset** オブジェクトのコピーを作成した場合、複製元および複製された **Recordset** の **Bookmark** プロパティの設定は同一になり、相互に使用することができます。一方、異なる **Recordset** オブジェクトのブックマークは、たとえ同一のソースまたは同一のコマンドから作成したものであっても、相互に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="5e146-p104">If you use the [Clone](clone-method-ado.md) method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and you can use them interchangeably. However, you cannot use bookmarks from different **Recordset** objects interchangeably, even if they were created from the same source or command.</span></span>

<span data-ttu-id="5e146-117">**リモートデータサービスの使用状況**クライアント側の**Recordset**オブジェクトで使用する場合、 **Bookmark**プロパティは常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="5e146-117">**Remote Data Service Usage**When used on a client-side **Recordset** object, the **Bookmark** property is always available.</span></span>

