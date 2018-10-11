---
title: フォルダー
TOCTitle: Folders
ms:assetid: b72b5705-d77a-4cad-873d-457b9fb6553e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184634(v=office.15)
ms:contentKeyID: 55119856
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: e0fd6aa6ff6a7c4d6c4821858aa8d2a3ca60b2c3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406429"
---
# <a name="folders"></a><span data-ttu-id="22cc3-102">フォルダー</span><span class="sxs-lookup"><span data-stu-id="22cc3-102">Folders</span></span>

<span data-ttu-id="22cc3-103">このセクションでは、フォルダーに関連するサンプル タスクを示します。</span><span class="sxs-lookup"><span data-stu-id="22cc3-103">This section provides sample tasks that involve views.</span></span> <span data-ttu-id="22cc3-104">[Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトは、Microsoft Outlook アイテムが保存されるフォルダーの階層構造を表します。</span><span class="sxs-lookup"><span data-stu-id="22cc3-104">[Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) objects represent the folder hierarchy where Microsoft Outlook items are stored.</span></span> <span data-ttu-id="22cc3-105">フォルダーの例として、[予定表]、[メール]、[削除済みアイテム] などのフォルダーが挙げられます。</span><span class="sxs-lookup"><span data-stu-id="22cc3-105">Examples of folders include the Calendar, Mail, and Deleted Items folders.</span></span> <span data-ttu-id="22cc3-106">Outlook プライマリ相互運用機能アセンブリ (PIA) では、**Folder** オブジェクトのメンバーが、[MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) オブジェクトのメンバーとして公開されています。</span><span class="sxs-lookup"><span data-stu-id="22cc3-106">In the Outlook Primary Interop Assembly (PIA), members of the **Folder** object are exposed as members of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="22cc3-107">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="22cc3-107">In this section</span></span>

|<span data-ttu-id="22cc3-108">トピック</span><span class="sxs-lookup"><span data-stu-id="22cc3-108">Topic</span></span>|<span data-ttu-id="22cc3-109">説明</span><span class="sxs-lookup"><span data-stu-id="22cc3-109">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="22cc3-110">フォルダー一覧にフォルダーを追加する</span><span class="sxs-lookup"><span data-stu-id="22cc3-110">Add a folder to the folder list</span></span>](how-to-add-a-folder-to-the-folder-list.md) |<span data-ttu-id="22cc3-111">[Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) メソッドを使用して、Outlook のフォルダー一覧にフォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="22cc3-111">Uses the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add a folder to the Outlook folder list.</span></span>|
|[<span data-ttu-id="22cc3-112">フォルダーを列挙する</span><span class="sxs-lookup"><span data-stu-id="22cc3-112">Enumerate folders</span></span>](how-to-enumerate-folders.md)  |<span data-ttu-id="22cc3-113">フォルダーのコレクションに対して順に処理を行い、フォルダーを列挙します。</span><span class="sxs-lookup"><span data-stu-id="22cc3-113">Enumerates folders by iterating through a collection of folders.</span></span>|
|[<span data-ttu-id="22cc3-114">既定のフォルダーを取得して、そのサブフォルダーを列挙する</span><span class="sxs-lookup"><span data-stu-id="22cc3-114">Get a default folder and enumerate its subfolders</span></span>](how-to-get-a-default-folder-and-enumerate-its-subfolders.md) |<span data-ttu-id="22cc3-115">ユーザーの既定のストアで既定のフォルダーを取得し、そのサブフォルダーを列挙します。</span><span class="sxs-lookup"><span data-stu-id="22cc3-115">Obtains a default folder in the user’s default store and enumerates its subfolders.</span></span>|
|[<span data-ttu-id="22cc3-116">フォルダーのパスに基づいてフォルダーを取得する</span><span class="sxs-lookup"><span data-stu-id="22cc3-116">Get a folder based on its folder path</span></span>](how-to-get-a-folder-based-on-its-folder-path.md)  |<span data-ttu-id="22cc3-117">フォルダーのパスを取得することで、関連するフォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="22cc3-117">Takes a folder path and obtains the associated folder.</span></span>|
|[<span data-ttu-id="22cc3-118">フォルダーを選択してフォルダーの情報を表示する</span><span class="sxs-lookup"><span data-stu-id="22cc3-118">Select a folder and display folder information</span></span>](how-to-select-a-folder-and-display-folder-information.md)  |<span data-ttu-id="22cc3-119">指定のフォルダー一覧からユーザーが選択するフォルダーについての情報をプログラムで表示します。</span><span class="sxs-lookup"><span data-stu-id="22cc3-119">Programmatically displays information about a folder that a user selects from a specified folder list.</span></span>|
|[<span data-ttu-id="22cc3-120">フォルダーの既定のメッセージ クラスを取得する</span><span class="sxs-lookup"><span data-stu-id="22cc3-120">Get the default message class of a folder</span></span>](how-to-get-the-default-message-class-of-a-folder.md)  |<span data-ttu-id="22cc3-121">[DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) プロパティを使用して、フォルダーの既定のメッセージ クラスを取得します。</span><span class="sxs-lookup"><span data-stu-id="22cc3-121">Uses the [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) property to obtain the default message class of a folder.</span></span>|
|[<span data-ttu-id="22cc3-122">非表示メッセージとしてフォルダーに格納されているソリューション固有のデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="22cc3-122">Access solution-specific data stored as a hidden message in a folder</span></span>](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)  |<span data-ttu-id="22cc3-123">[StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) オブジェクトを使用して、特定のメッセージ クラスの非表示メッセージとしてフォルダーに格納されているデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="22cc3-123">Uses the [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) object to retrieve data that is stored as a hidden message of a specific message class in a folder.</span></span>|
|[<span data-ttu-id="22cc3-124">フォルダー レベルのクエリでカスタム アイテム プロパティが確実にサポートされるようにする</span><span class="sxs-lookup"><span data-stu-id="22cc3-124">Ensure that custom item properties are supported in folder-level queries</span></span>](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md) |<span data-ttu-id="22cc3-125">あるアイテム型にカスタム プロパティを追加した場合に、フォルダーにもそのプロパティを追加して、フォルダー レベルでそのカスタム プロパティに対するクエリを実行できるようにする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="22cc3-125">Shows how to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>|

## <a name="see-also"></a><span data-ttu-id="22cc3-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="22cc3-126">See also</span></span>

- [<span data-ttu-id="22cc3-127">予定表</span><span class="sxs-lookup"><span data-stu-id="22cc3-127">Calendar</span></span>](calendar.md)
- [<span data-ttu-id="22cc3-128">連絡先</span><span class="sxs-lookup"><span data-stu-id="22cc3-128">Contacts</span></span>](contacts.md)
- [<span data-ttu-id="22cc3-129">メール</span><span class="sxs-lookup"><span data-stu-id="22cc3-129">Mail</span></span>](mail.md)
- [<span data-ttu-id="22cc3-130">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="22cc3-130">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

