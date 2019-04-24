---
title: Folders
TOCTitle: Folders
ms:assetid: b72b5705-d77a-4cad-873d-457b9fb6553e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184634(v=office.15)
ms:contentKeyID: 55119856
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecf342c54d1aa2020fbfad4175a220b2aefecbe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327183"
---
# <a name="folders"></a><span data-ttu-id="fa370-102">フォルダー</span><span class="sxs-lookup"><span data-stu-id="fa370-102">Folders</span></span>

<span data-ttu-id="fa370-p101">This section provides sample tasks that involve folders. [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) objects represent the folder hierarchy where Microsoft Outlook items are stored. Examples of folders include the Calendar, Mail, and Deleted Items folders. In the Outlook Primary Interop Assembly (PIA), members of the **Folder** object are exposed as members of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.</span><span class="sxs-lookup"><span data-stu-id="fa370-p101">This section provides sample tasks that involve folders. [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) objects represent the folder hierarchy where Microsoft Outlook items are stored. Examples of folders include the Calendar, Mail, and Deleted Items folders. In the Outlook Primary Interop Assembly (PIA), members of the **Folder** object are exposed as members of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fa370-107">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="fa370-107">In this section</span></span>

|<span data-ttu-id="fa370-108">トピック</span><span class="sxs-lookup"><span data-stu-id="fa370-108">Topic</span></span>|<span data-ttu-id="fa370-109">説明</span><span class="sxs-lookup"><span data-stu-id="fa370-109">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="fa370-110">フォルダー一覧にフォルダーを追加する</span><span class="sxs-lookup"><span data-stu-id="fa370-110">Add a folder to the folder list</span></span>](how-to-add-a-folder-to-the-folder-list.md) |<span data-ttu-id="fa370-111">[Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) メソッドを使用して、Outlook のフォルダー一覧にフォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="fa370-111">Uses the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add a folder to the Outlook folder list.</span></span>|
|[<span data-ttu-id="fa370-112">フォルダーを列挙する</span><span class="sxs-lookup"><span data-stu-id="fa370-112">Enumerate folders</span></span>](how-to-enumerate-folders.md)  |<span data-ttu-id="fa370-113">フォルダーのコレクションに対して順に処理を行い、フォルダーを列挙します。</span><span class="sxs-lookup"><span data-stu-id="fa370-113">Enumerates folders by iterating through a collection of folders.</span></span>|
|[<span data-ttu-id="fa370-114">既定のフォルダーを取得して、そのサブフォルダーを列挙する</span><span class="sxs-lookup"><span data-stu-id="fa370-114">Get a default folder and enumerate its subfolders</span></span>](how-to-get-a-default-folder-and-enumerate-its-subfolders.md) |<span data-ttu-id="fa370-115">ユーザーの既定のストアで既定のフォルダーを取得し、そのサブフォルダーを列挙します。</span><span class="sxs-lookup"><span data-stu-id="fa370-115">Obtains a default folder in the user’s default store and enumerates its subfolders.</span></span>|
|[<span data-ttu-id="fa370-116">フォルダーのパスに基づいてフォルダーを取得する</span><span class="sxs-lookup"><span data-stu-id="fa370-116">Get a folder based on its folder path</span></span>](how-to-get-a-folder-based-on-its-folder-path.md)  |<span data-ttu-id="fa370-117">フォルダーのパスを取得することで、関連するフォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="fa370-117">Takes a folder path and obtains the associated folder.</span></span>|
|[<span data-ttu-id="fa370-118">フォルダーを選択してフォルダーの情報を表示する</span><span class="sxs-lookup"><span data-stu-id="fa370-118">Select a folder and display folder information</span></span>](how-to-select-a-folder-and-display-folder-information.md)  |<span data-ttu-id="fa370-119">指定のフォルダー一覧からユーザーが選択するフォルダーについての情報をプログラムで表示します。</span><span class="sxs-lookup"><span data-stu-id="fa370-119">Programmatically displays information about a folder that a user selects from a specified folder list.</span></span>|
|[<span data-ttu-id="fa370-120">フォルダーの既定のメッセージ クラスを取得する</span><span class="sxs-lookup"><span data-stu-id="fa370-120">Get the default message class of a folder</span></span>](how-to-get-the-default-message-class-of-a-folder.md)  |<span data-ttu-id="fa370-121">[DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) プロパティを使用して、フォルダーの既定のメッセージ クラスを取得します。</span><span class="sxs-lookup"><span data-stu-id="fa370-121">Uses the [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) property to obtain the default message class of a folder.</span></span>|
|[<span data-ttu-id="fa370-122">非表示メッセージとしてフォルダーに格納されているソリューション固有のデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="fa370-122">Access solution-specific data stored as a hidden message in a folder</span></span>](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)  |<span data-ttu-id="fa370-123">[StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) オブジェクトを使用して、特定のメッセージ クラスの非表示メッセージとしてフォルダーに格納されているデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="fa370-123">Uses the [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) object to retrieve data that is stored as a hidden message of a specific message class in a folder.</span></span>|
|[<span data-ttu-id="fa370-124">フォルダー レベルのクエリでカスタム アイテム プロパティが確実にサポートされるようにする</span><span class="sxs-lookup"><span data-stu-id="fa370-124">Ensure that custom item properties are supported in folder-level queries</span></span>](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md) |<span data-ttu-id="fa370-125">あるアイテム型にカスタム プロパティを追加した場合に、フォルダーにもそのプロパティを追加して、フォルダー レベルでそのカスタム プロパティに対するクエリを実行できるようにする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="fa370-125">Shows how to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>|

## <a name="see-also"></a><span data-ttu-id="fa370-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa370-126">See also</span></span>

- [<span data-ttu-id="fa370-127">予定表</span><span class="sxs-lookup"><span data-stu-id="fa370-127">Calendar</span></span>](calendar.md)
- [<span data-ttu-id="fa370-128">連絡先</span><span class="sxs-lookup"><span data-stu-id="fa370-128">Contacts</span></span>](contacts.md)
- [<span data-ttu-id="fa370-129">メール</span><span class="sxs-lookup"><span data-stu-id="fa370-129">Mail</span></span>](mail.md)
- [<span data-ttu-id="fa370-130">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="fa370-130">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

