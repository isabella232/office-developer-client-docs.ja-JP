---
title: 連絡先
TOCTitle: Contacts
ms:assetid: e988de54-6b1e-4e83-a226-3a898903608f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184649(v=office.15)
ms:contentKeyID: 55119820
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e8a524e6cd7fbc4fdb2818279a9975b0813de886
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350982"
---
# <a name="contacts"></a><span data-ttu-id="25f17-102">連絡先</span><span class="sxs-lookup"><span data-stu-id="25f17-102">Contacts</span></span>

<span data-ttu-id="25f17-103">このセクションでは、連絡先に関連するサンプル トピックを示します。</span><span class="sxs-lookup"><span data-stu-id="25f17-103">This section provides sample topics that involve contacts.</span></span> <span data-ttu-id="25f17-104">連絡先とは、やり取りを行うユーザーや企業のことです。</span><span class="sxs-lookup"><span data-stu-id="25f17-104">Contacts represent people and businesses you want to communicate with.</span></span> <span data-ttu-id="25f17-105">連絡先フォルダーはメール アドレス帳であり、連絡先の情報の格納場所でもあります。</span><span class="sxs-lookup"><span data-stu-id="25f17-105">The Contacts folder is your email address book and information storage for the contacts.</span></span> <span data-ttu-id="25f17-106">[ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) オブジェクトは、連絡先フォルダー内の一意の連絡先を表す Outlook の組み込みオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="25f17-106">A [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object is an Outlook built-in object that represents unique contacts in a Contacts folder.</span></span> <span data-ttu-id="25f17-107">**ContactItem** オブジェクトには、[FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\))、[CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\))、[OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)) などの 100 以上のプロパティが存在します。また、組み込みプロパティが不十分な場合、カスタム プロパティに各連絡先の情報を格納できます。</span><span class="sxs-lookup"><span data-stu-id="25f17-107">The **ContactItem** object has over 100 properties, such as [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), and [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)), as well as custom properties if the built-in properties are not sufficient, that you can use to store information about each contact.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="25f17-108">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="25f17-108">In this section</span></span>

|<span data-ttu-id="25f17-109">トピック</span><span class="sxs-lookup"><span data-stu-id="25f17-109">Topic</span></span>|<span data-ttu-id="25f17-110">説明</span><span class="sxs-lookup"><span data-stu-id="25f17-110">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="25f17-111">連絡先アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="25f17-111">Create a Contact item</span></span>](how-to-create-a-contact-item.md)  |<span data-ttu-id="25f17-112">連絡先アイテムを作成し、連絡先のさまざまなプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="25f17-112">Creates a contact item and sets various properties for the contact.</span></span>|
|[<span data-ttu-id="25f17-113">カスタムの連絡先アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="25f17-113">Create a custom Contact item</span></span>](how-to-create-a-custom-contact-item.md)  |<span data-ttu-id="25f17-114">カスタム連絡先アイテムを作成し、あらかじめ定義されたプロパティとユーザー定義のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="25f17-114">Creates a custom contact item and sets both predefined and user-defined properties.</span></span>|
|[<span data-ttu-id="25f17-115">vCard ファイルから連絡先アイテムを作成し、フォルダーにアイテムを保存する</span><span class="sxs-lookup"><span data-stu-id="25f17-115">Create a Contact item from a vCard file and save the item in a folder</span></span>](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)  |<span data-ttu-id="25f17-116">ファイル システムのフォルダーに入っているすべての vCard ファイルをインポートし、連絡先を *targetFolder* パラメーターで指定されたフォルダーに保存します。</span><span class="sxs-lookup"><span data-stu-id="25f17-116">Imports all the vCard files in a file system folder and saves the contacts into the folder specified by the *targetFolder* parameter.</span></span>|

## <a name="see-also"></a><span data-ttu-id="25f17-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="25f17-117">See also</span></span>

- [<span data-ttu-id="25f17-118">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="25f17-118">Address book</span></span>](address-book.md)
- [<span data-ttu-id="25f17-119">電子名刺</span><span class="sxs-lookup"><span data-stu-id="25f17-119">Electronic business cards</span></span>](electronic-business-cards.md)
- [<span data-ttu-id="25f17-120">メール</span><span class="sxs-lookup"><span data-stu-id="25f17-120">Mail</span></span>](mail.md)
- [<span data-ttu-id="25f17-121">受信者</span><span class="sxs-lookup"><span data-stu-id="25f17-121">Recipients</span></span>](recipients.md)
- [<span data-ttu-id="25f17-122">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="25f17-122">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

