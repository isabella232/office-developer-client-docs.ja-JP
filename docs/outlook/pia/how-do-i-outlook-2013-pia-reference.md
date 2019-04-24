---
title: 操作方法 (Outlook 2013 PIA リファレンス)
TOCTitle: How do I...
ms:assetid: ff647d52-bd32-4945-afa4-5b97d9a0d7dd
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612741(v=office.15)
ms:contentKeyID: 55119792
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bc4e19271e2747f5ffa8586b9f2ab226d6658b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355798"
---
# <a name="how-do-i-outlook-2013-pia-reference"></a><span data-ttu-id="502cb-102">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="502cb-102">How do I... (Outlook 2013 PIA reference)</span></span>

<span data-ttu-id="502cb-103">このセクションにはタスク関連のトピックがまとめられています。ここでは、Outlook でよく使われる機能の実行方法を Visual Basic と C\# のコード例で示します。</span><span class="sxs-lookup"><span data-stu-id="502cb-103">This section contains procedural tasks topics and code examples in Visual Basic and C\# that demonstrate how to perform some common tasks in Outlook.</span></span>

<span data-ttu-id="502cb-104">これらのコード例を実行するには、Outlook 2010 と Visual Studio 2008、またはこれらの製品の新しいバージョンのインストールを完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="502cb-104">To run these code examples, you must have installed Outlook 2010 and Visual Studio 2008, or a later version of these products.</span></span>

<span data-ttu-id="502cb-105">このセクションのコード例では、Visual Studio の Office Developer Tools がインストールされている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="502cb-105">The code examples in this section do not require that you have installed Office Developer Tools for Visual Studio.</span></span> <span data-ttu-id="502cb-106">ただし、ツールの使用についての詳細は [Office の開発を開始する](https://developer.microsoft.com/office/docs) ポータルを参照し、マネージ コードで書かれたいくつかの基本的な使い方に関するタスクについては 「[Outlook ソリューション](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017)」を参照していただけます。</span><span class="sxs-lookup"><span data-stu-id="502cb-106">However, you can refer to the [Getting started with Office development](https://developer.microsoft.com/office/docs) portal for information about using the tools, and refer to [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) for some basic how-to tasks written in managed code.</span></span>

<span data-ttu-id="502cb-107">このセクションのコード例には、初心者から中級者向けの例が含まれており、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493)』から抜粋した例も一部含まれています。</span><span class="sxs-lookup"><span data-stu-id="502cb-107">Code examples in this section range from the beginner to the intermediate levels, and some of them are adapted from the book [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).</span></span>

<span data-ttu-id="502cb-108">タスクのアイデアやコード サンプルがございましたらぜひ Office 開発者向けドキュメント チームへお寄せください。</span><span class="sxs-lookup"><span data-stu-id="502cb-108">The Office Developer Documentation team welcomes your task ideas and code samples.</span></span> <span data-ttu-id="502cb-109">お寄せいただいたコード サンプルを Outlook コンテンツで使用する場合は、お客様の署名とお客様の Web サイトへのリンクを記載してそれがお客様のものであることを案内します。</span><span class="sxs-lookup"><span data-stu-id="502cb-109">If we use your code samples in Outlook content, we will recognize your work with a byline and a link to your website.</span></span> <span data-ttu-id="502cb-110">詳細については、docthis@microsoft.com にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="502cb-110">For more information, contact us at docthis@microsoft.com.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="502cb-111">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="502cb-111">In this section</span></span> 

[<span data-ttu-id="502cb-112">アカウント</span><span class="sxs-lookup"><span data-stu-id="502cb-112">Accounts</span></span>](accounts.md)

- [<span data-ttu-id="502cb-113">アカウント情報を取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-113">Get account information</span></span>](how-to-get-account-information.md)
- [<span data-ttu-id="502cb-114">現在のフォルダーに基づいて特定のアカウントの送信可能なアイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-114">Create a sendable item for a specific account based on the current folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [<span data-ttu-id="502cb-115">フォルダーのアカウントを取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-115">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md)
- [<span data-ttu-id="502cb-116">複数のアカウントの情報を取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-116">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md)
- [<span data-ttu-id="502cb-117">Hotmail アカウントを使用してメール アイテムを送信する</span><span class="sxs-lookup"><span data-stu-id="502cb-117">Send a mail item by using a Hotmail account</span></span>](how-to-send-a-mail-item-by-using-a-hotmail-account.md)

[<span data-ttu-id="502cb-118">アドイン管理</span><span class="sxs-lookup"><span data-stu-id="502cb-118">Add-in administration</span></span>](add-in-administration.md)

- [<span data-ttu-id="502cb-119">コンピューター上で Outlook がクイック実行アプリケーションかどうかを確認する</span><span class="sxs-lookup"><span data-stu-id="502cb-119">Determine whether Outlook is a Click-to-Run application on a computer</span></span>](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[<span data-ttu-id="502cb-120">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="502cb-120">Address book</span></span>](address-book.md)

- <span data-ttu-id="502cb-121">[Contacts フォルダーに対応するアドレス帳を [名前の選択] ダイアログ ボックスに表示する](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)</span><span class="sxs-lookup"><span data-stu-id="502cb-121">[Display in the Select Names dialog box the address book corresponding to a Contacts folder](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)</span></span>
- [<span data-ttu-id="502cb-122">ストアのグローバル アドレス一覧またはアドレス一覧のセットを取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-122">Get the Global Address List or a set of address lists for a store</span></span>](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [<span data-ttu-id="502cb-123">グローバル アドレス一覧のエントリを列挙する</span><span class="sxs-lookup"><span data-stu-id="502cb-123">Enumerate the entries in the Global Address List</span></span>](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [<span data-ttu-id="502cb-124">プロファイルのアドレス一覧を表示する</span><span class="sxs-lookup"><span data-stu-id="502cb-124">Display the address lists for a profile</span></span>](how-to-display-the-address-lists-for-a-profile.md)

[<span data-ttu-id="502cb-125">予定</span><span class="sxs-lookup"><span data-stu-id="502cb-125">Appointments</span></span>](appointments.md)

- [<span data-ttu-id="502cb-126">終日イベントの予定を作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-126">Create an appointment that is an all-day event</span></span>](how-to-create-an-appointment-that-is-an-all-day-event.md)
- [<span data-ttu-id="502cb-127">太平洋タイム ゾーンで開始して東部タイム ゾーンで終了する予定を作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-127">Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone</span></span>](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- [<span data-ttu-id="502cb-128">予定アイテムに異なる受信者の種類を指定する</span><span class="sxs-lookup"><span data-stu-id="502cb-128">Specify different recipient types for an appointment item</span></span>](how-to-specify-different-recipient-types-for-an-appointment-item.md)
- [<span data-ttu-id="502cb-129">既定の定期的なパターンを使用して、定期的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-129">Create a recurring appointment by using the default recurrence pattern</span></span>](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [<span data-ttu-id="502cb-130">週単位パターンの定期的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-130">Create a recurring appointment that has a weekly pattern</span></span>](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [<span data-ttu-id="502cb-131">YearNth パターンの年単位の定期的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-131">Create an annual recurring appointment that uses a YearNth pattern</span></span>](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [<span data-ttu-id="502cb-132">定期的な一連の予定から特定の予定を検索する</span><span class="sxs-lookup"><span data-stu-id="502cb-132">Find a specific appointment in a recurring appointment series</span></span>](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="502cb-133">定期的な一連の予定に例外的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-133">Create an exception appointment in a recurring appointment series</span></span>](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="502cb-134">予定アイテムのリマインダーを作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-134">Create a reminder for an appointment item</span></span>](how-to-create-a-reminder-for-an-appointment-item.md)
- [<span data-ttu-id="502cb-135">予定の XML データを Outlook の予定オブジェクトにインポートする</span><span class="sxs-lookup"><span data-stu-id="502cb-135">Import appointment XML data into Outlook appointment objects</span></span>](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[<span data-ttu-id="502cb-136">添付ファイル</span><span class="sxs-lookup"><span data-stu-id="502cb-136">Attachments</span></span>](attachments.md)

- [<span data-ttu-id="502cb-137">メール アイテムにファイルを添付する</span><span class="sxs-lookup"><span data-stu-id="502cb-137">Attach a file to a mail item</span></span>](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [<span data-ttu-id="502cb-138">Outlook の連絡先アイテムを電子メール メッセージに添付する</span><span class="sxs-lookup"><span data-stu-id="502cb-138">Attach an Outlook Contact item to an email message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [<span data-ttu-id="502cb-139">Outlook 電子メール メッセージの添付ファイルのサイズを制限する</span><span class="sxs-lookup"><span data-stu-id="502cb-139">Limit the size of an attachment to an Outlook email message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [<span data-ttu-id="502cb-140">Outlook 電子メール メッセージの添付ファイルを変更する</span><span class="sxs-lookup"><span data-stu-id="502cb-140">Modify an attachment of an Outlook email message</span></span>](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [<span data-ttu-id="502cb-141">プログラムでメッセージからセキュリティ レベル 2 の添付ファイルを削除してディスクに保存する</span><span class="sxs-lookup"><span data-stu-id="502cb-141">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[<span data-ttu-id="502cb-142">Calendar</span><span class="sxs-lookup"><span data-stu-id="502cb-142">Calendar</span></span>](calendar.md)

- [<span data-ttu-id="502cb-143">予定表で指定した期間内の空き時間スケジュールを共有する</span><span class="sxs-lookup"><span data-stu-id="502cb-143">Share Free/Busy schedule within a specified period in a calendar</span></span>](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [<span data-ttu-id="502cb-144">電子メールで予定表情報を共有する</span><span class="sxs-lookup"><span data-stu-id="502cb-144">Share calendar information through email</span></span>](how-to-share-calendar-information-through-e-mail.md)
- [<span data-ttu-id="502cb-145">受信者の共有の予定表を表示する</span><span class="sxs-lookup"><span data-stu-id="502cb-145">Display a shared calendar of a recipient</span></span>](how-to-display-a-shared-calendar-of-a-recipient.md)
- [<span data-ttu-id="502cb-146">予定表をディスクに保存する</span><span class="sxs-lookup"><span data-stu-id="502cb-146">Save a calendar to disk</span></span>](how-to-save-a-calendar-to-disk.md)
- [<span data-ttu-id="502cb-147">iCalendar ファイルを開いて内容を表示する</span><span class="sxs-lookup"><span data-stu-id="502cb-147">Open and display the contents of an iCalendar file</span></span>](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[<span data-ttu-id="502cb-148">色の分類項目</span><span class="sxs-lookup"><span data-stu-id="502cb-148">Color categories</span></span>](color-categories.md)

- [<span data-ttu-id="502cb-149">分類項目を列挙および追加する</span><span class="sxs-lookup"><span data-stu-id="502cb-149">Enumerate and add categories</span></span>](how-to-enumerate-and-add-categories.md)
- [<span data-ttu-id="502cb-150">分類項目をアイテムに割り当てる</span><span class="sxs-lookup"><span data-stu-id="502cb-150">Assign categories to an item</span></span>](how-to-assign-categories-to-an-item.md)

[<span data-ttu-id="502cb-151">連絡先</span><span class="sxs-lookup"><span data-stu-id="502cb-151">Contacts</span></span>](contacts.md)

- [<span data-ttu-id="502cb-152">連絡先アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-152">Create a Contact item</span></span>](how-to-create-a-contact-item.md)
- [<span data-ttu-id="502cb-153">カスタムの連絡先アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-153">Create a custom Contact item</span></span>](how-to-create-a-custom-contact-item.md)
- [<span data-ttu-id="502cb-154">vCard ファイルから連絡先アイテムを作成し、フォルダーにアイテムを保存する</span><span class="sxs-lookup"><span data-stu-id="502cb-154">Create a Contact item from a vCard file and save the item in a folder</span></span>](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[<span data-ttu-id="502cb-155">会話</span><span class="sxs-lookup"><span data-stu-id="502cb-155">Conversations</span></span>](conversations.md)

- [<span data-ttu-id="502cb-156">スレッド内のアイテムを取得して表示する</span><span class="sxs-lookup"><span data-stu-id="502cb-156">Get and display items in a conversation</span></span>](how-to-get-and-display-items-in-a-conversation.md)
- [<span data-ttu-id="502cb-157">選択されたスレッドを取得して列挙する</span><span class="sxs-lookup"><span data-stu-id="502cb-157">Get and enumerate selected conversations</span></span>](how-to-get-and-enumerate-selected-conversations.md)

[<span data-ttu-id="502cb-158">電子名刺</span><span class="sxs-lookup"><span data-stu-id="502cb-158">Electronic business cards</span></span>](electronic-business-cards.md)

- [<span data-ttu-id="502cb-159">電子名刺のレイアウトを変更する</span><span class="sxs-lookup"><span data-stu-id="502cb-159">Modify the layout of an electronic business card</span></span>](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [<span data-ttu-id="502cb-160">電子名刺付きのメール アイテムを送信する</span><span class="sxs-lookup"><span data-stu-id="502cb-160">Send a mail item with an electronic business card</span></span>](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[<span data-ttu-id="502cb-161">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="502cb-161">Exchange users</span></span>](exchange-users.md)

- [<span data-ttu-id="502cb-162">現在のユーザーの情報を取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-162">Get information about the current user</span></span>](how-to-get-information-about-the-current-user.md)
- [<span data-ttu-id="502cb-163">現在のユーザーがメンバーになっているすべての配布リストについての情報を取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-163">Get information about all distribution lists of which the current user is a member</span></span>](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [<span data-ttu-id="502cb-164">配布リストを作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-164">Create a distribution list</span></span>](how-to-create-a-distribution-list.md)
- [<span data-ttu-id="502cb-165">Exchange 配布リストのメンバーを取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-165">Get members of an Exchange distribution list</span></span>](how-to-get-members-of-an-exchange-distribution-list.md)
- [<span data-ttu-id="502cb-166">現在のユーザーの上司の情報を取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-166">Get information about the current user's manager</span></span>](how-to-get-information-about-the-current-user-s-manager.md)
- [<span data-ttu-id="502cb-167">Exchange ユーザーの上司の空き時間情報を取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-167">Get availability information for an Exchange user's manager</span></span>](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [<span data-ttu-id="502cb-168">会議出席依頼に対する上司からの返信を確認する</span><span class="sxs-lookup"><span data-stu-id="502cb-168">Check a manager's response to a meeting request</span></span>](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [<span data-ttu-id="502cb-169">現在のユーザーの上司の直属部下についての情報を取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-169">Get information about direct reports of the current user's manager</span></span>](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[<span data-ttu-id="502cb-170">フォルダー</span><span class="sxs-lookup"><span data-stu-id="502cb-170">Folders</span></span>](folders.md)

- [<span data-ttu-id="502cb-171">フォルダー一覧にフォルダーを追加する</span><span class="sxs-lookup"><span data-stu-id="502cb-171">Add a folder to the folder list</span></span>](how-to-add-a-folder-to-the-folder-list.md)
- [<span data-ttu-id="502cb-172">フォルダーを列挙する</span><span class="sxs-lookup"><span data-stu-id="502cb-172">Enumerate folders</span></span>](how-to-enumerate-folders.md)
- [<span data-ttu-id="502cb-173">既定のフォルダーを取得して、そのサブフォルダーを列挙する</span><span class="sxs-lookup"><span data-stu-id="502cb-173">Get a default folder and enumerate its subfolders</span></span>](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [<span data-ttu-id="502cb-174">フォルダーのパスに基づいてフォルダーを取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-174">Get a folder based on its folder path</span></span>](how-to-get-a-folder-based-on-its-folder-path.md)
- [<span data-ttu-id="502cb-175">フォルダーを選択してフォルダーの情報を表示する</span><span class="sxs-lookup"><span data-stu-id="502cb-175">Select a folder and display folder information</span></span>](how-to-select-a-folder-and-display-folder-information.md)
- [<span data-ttu-id="502cb-176">フォルダーの既定のメッセージ クラスを取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-176">Get the default message class of a folder</span></span>](how-to-get-the-default-message-class-of-a-folder.md)
- [<span data-ttu-id="502cb-177">非表示メッセージとしてフォルダーに格納されているソリューション固有のデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="502cb-177">Access solution-specific data stored as a hidden message in a folder</span></span>](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [<span data-ttu-id="502cb-178">フォルダー レベルのクエリでカスタム アイテム プロパティが確実にサポートされるようにする</span><span class="sxs-lookup"><span data-stu-id="502cb-178">Ensure that custom item properties are supported in folder-level queries</span></span>](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[<span data-ttu-id="502cb-179">Outlook アイテム全般</span><span class="sxs-lookup"><span data-stu-id="502cb-179">General Outlook items</span></span>](general-outlook-items.md)

- [<span data-ttu-id="502cb-180">ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする</span><span class="sxs-lookup"><span data-stu-id="502cb-180">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="502cb-181">アクティブ エクスプローラーで選択した項目を表示する</span><span class="sxs-lookup"><span data-stu-id="502cb-181">Display selected items in the active Explorer</span></span>](how-to-display-selected-items-in-the-active-explorer.md)

[<span data-ttu-id="502cb-182">グループ共有</span><span class="sxs-lookup"><span data-stu-id="502cb-182">Group sharing</span></span>](group-sharing.md)

- [<span data-ttu-id="502cb-183">RSS フィードを購読する</span><span class="sxs-lookup"><span data-stu-id="502cb-183">Subscribe to an RSS feed</span></span>](how-to-subscribe-to-an-rss-feed.md)
- [<span data-ttu-id="502cb-184">Outlook と SharePoint のフォルダーを同期させる</span><span class="sxs-lookup"><span data-stu-id="502cb-184">Synchronize Outlook with a SharePoint folder</span></span>](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[<span data-ttu-id="502cb-185">メール</span><span class="sxs-lookup"><span data-stu-id="502cb-185">Mail</span></span>](mail.md)

- [<span data-ttu-id="502cb-186">メッセージ テンプレートを使用してメール アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-186">Create a mail item by using a message template</span></span>](how-to-create-a-mail-item-by-using-a-message-template.md)
- [<span data-ttu-id="502cb-187">メール アイテムを作成し、レポートを添付して、ユーザーの上司にメール アイテムを送信する</span><span class="sxs-lookup"><span data-stu-id="502cb-187">Create a mail item, attach a report, and send the mail item to the user's manager</span></span>](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [<span data-ttu-id="502cb-188">アカウントの SMTP アドレスを指定して電子メールを送信する</span><span class="sxs-lookup"><span data-stu-id="502cb-188">Send an email given the SMTP address of an account</span></span>](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [<span data-ttu-id="502cb-189">メール アイテムに投票オプションを追加する</span><span class="sxs-lookup"><span data-stu-id="502cb-189">Add voting options to a mail item</span></span>](how-to-add-voting-options-to-a-mail-item.md)
- [<span data-ttu-id="502cb-190">メール アイテムへの返信として行うカスタム アクションを追加する</span><span class="sxs-lookup"><span data-stu-id="502cb-190">Add a custom action as a response to a mail item</span></span>](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [<span data-ttu-id="502cb-191">メール アイテムの差出人の SMTP アドレスを取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-191">Get the SMTP address of the sender of a mail item</span></span>](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [<span data-ttu-id="502cb-192">メール アイテムのさまざまな受信者の種類を指定する</span><span class="sxs-lookup"><span data-stu-id="502cb-192">Specify different recipient types for a mail item</span></span>](how-to-specify-different-recipient-types-for-a-mail-item.md)

[<span data-ttu-id="502cb-193">会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="502cb-193">Meeting requests</span></span>](meeting-requests.md)

- [<span data-ttu-id="502cb-194">会議出席依頼を作成し、受信者を追加して、場所を指定する</span><span class="sxs-lookup"><span data-stu-id="502cb-194">Create a meeting request, add recipients, and specify a location</span></span>](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [<span data-ttu-id="502cb-195">会議の開催者を取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-195">Get the organizer of a meeting</span></span>](how-to-get-the-organizer-of-a-meeting.md)
- [<span data-ttu-id="502cb-196">会議出席依頼へのすべての返信を調べる</span><span class="sxs-lookup"><span data-stu-id="502cb-196">Check all responses to a meeting request</span></span>](how-to-check-all-responses-to-a-meeting-request.md)
- [<span data-ttu-id="502cb-197">会議出席依頼に関連付けられている予定アイテムを検索する</span><span class="sxs-lookup"><span data-stu-id="502cb-197">Find the appointment item associated with a meeting request</span></span>](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [<span data-ttu-id="502cb-198">会議出席依頼を自動的に承諾する</span><span class="sxs-lookup"><span data-stu-id="502cb-198">Automatically accept a meeting request</span></span>](how-to-automatically-accept-a-meeting-request.md)
- [<span data-ttu-id="502cb-199">会議出席依頼への返信をユーザーに求める</span><span class="sxs-lookup"><span data-stu-id="502cb-199">Prompt a user to respond to a meeting request</span></span>](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[<span data-ttu-id="502cb-200">受信者</span><span class="sxs-lookup"><span data-stu-id="502cb-200">Recipients</span></span>](recipients.md)

- <span data-ttu-id="502cb-201">[[名前の選択] ダイアログ ボックスを表示して受信者を解決する](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)</span><span class="sxs-lookup"><span data-stu-id="502cb-201">[Display the Select Names dialog box to resolve recipients](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)</span></span>
- <span data-ttu-id="502cb-202">[[名前の選択] ダイアログ ボックスを使用して、受信者を取得し、予定に割り当てる](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)</span><span class="sxs-lookup"><span data-stu-id="502cb-202">[Use the Select Names dialog box to obtain and assign recipients to an appointment](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)</span></span>
- [<span data-ttu-id="502cb-203">受信者のメール アドレス</span><span class="sxs-lookup"><span data-stu-id="502cb-203">Get the email address of a recipient</span></span>](how-to-get-the-e-mail-address-of-a-recipient.md)

[<span data-ttu-id="502cb-204">ルール</span><span class="sxs-lookup"><span data-stu-id="502cb-204">Rules</span></span>](rules.md)

- [<span data-ttu-id="502cb-205">上司からのメール アイテムを分類して確認のフラグを設定する</span><span class="sxs-lookup"><span data-stu-id="502cb-205">Create a rule to file mail items from a manager and flag them for follow-up</span></span>](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [<span data-ttu-id="502cb-206">ルールを直ちに実行する</span><span class="sxs-lookup"><span data-stu-id="502cb-206">Execute a rule instantly</span></span>](how-to-execute-a-rule-instantly.md)
- [<span data-ttu-id="502cb-207">ローカル コンピューターでルールを実行する</span><span class="sxs-lookup"><span data-stu-id="502cb-207">Execute a rule on a local computer</span></span>](how-to-execute-a-rule-on-a-local-computer.md)
- [<span data-ttu-id="502cb-208">件名内の複数の単語に基づいてメール アイテムに分類項目を割り当てるルールを作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-208">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[<span data-ttu-id="502cb-209">Outlook のイベントを使用するサンプル タスク</span><span class="sxs-lookup"><span data-stu-id="502cb-209">Sample tasks using Outlook events</span></span>](sample-tasks-using-outlook-events.md)

- [<span data-ttu-id="502cb-210">インスペクターのラッパーを実装し、インスペクターごとにアイテム レベルのイベントを追跡する</span><span class="sxs-lookup"><span data-stu-id="502cb-210">Implement a wrapper for inspectors and track item-level events in each inspector</span></span>](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[<span data-ttu-id="502cb-211">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="502cb-211">Search and filter</span></span>](search-and-filter.md)

- [<span data-ttu-id="502cb-212">フォルダーのアイテムをフィルター処理して効率よく列挙する</span><span class="sxs-lookup"><span data-stu-id="502cb-212">Filter and efficiently enumerate items in a folder</span></span>](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="502cb-213">SetColumns を使用してフォルダーのアイテムを効率よく列挙する</span><span class="sxs-lookup"><span data-stu-id="502cb-213">Use SetColumns to efficiently enumerate items in a folder</span></span>](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="502cb-214">配列を使用してフォルダーのアイテムを効率よく列挙する</span><span class="sxs-lookup"><span data-stu-id="502cb-214">Use arrays to efficiently enumerate items in a folder</span></span>](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="502cb-215">最終変更時刻に基づいて受信トレイ内のアイテムを列挙する</span><span class="sxs-lookup"><span data-stu-id="502cb-215">Enumerate items in the Inbox based on the last modification time</span></span>](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [<span data-ttu-id="502cb-216">先月変更された受信トレイ アイテムをフィルター処理して表示する</span><span class="sxs-lookup"><span data-stu-id="502cb-216">Filter and display Inbox items modified in the last month</span></span>](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [<span data-ttu-id="502cb-217">フォルダー内のアイテムの列挙時に複数値プロパティをフィルター処理して表示する</span><span class="sxs-lookup"><span data-stu-id="502cb-217">Filter and display multivalued properties when enumerating items in a folder</span></span>](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="502cb-218">フォルダー内のアイテムの列挙時に、計算済みのプロパティをフィルター処理して表示する</span><span class="sxs-lookup"><span data-stu-id="502cb-218">Filter and display computed properties when enumerating items in a folder</span></span>](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="502cb-219">フォルダー内の非表示のアイテムを列挙する</span><span class="sxs-lookup"><span data-stu-id="502cb-219">Enumerate hidden items in a folder</span></span>](how-to-enumerate-hidden-items-in-a-folder.md)
- [<span data-ttu-id="502cb-220">クイック検索を使用して、すべてのフォルダーとすべてのストアから件名の特定の語句を検索する</span><span class="sxs-lookup"><span data-stu-id="502cb-220">Use instant search to search all folders and all stores for a phrase in the subject</span></span>](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [<span data-ttu-id="502cb-221">フォルダー内のアイテムの本文で語句を検索する</span><span class="sxs-lookup"><span data-stu-id="502cb-221">Search for a phrase in the body of items in a folder</span></span>](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [<span data-ttu-id="502cb-222">フォルダー内のアイテムの添付ファイルで完全に一致する語句を検索する</span><span class="sxs-lookup"><span data-stu-id="502cb-222">Search attachments of items in a folder for an exact phrase</span></span>](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [<span data-ttu-id="502cb-223">時間範囲内の予定を検索、取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-223">Search and obtain appointments in a time range</span></span>](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [<span data-ttu-id="502cb-224">定期的な予定でフィルター処理した後、件名の文字列を検索する</span><span class="sxs-lookup"><span data-stu-id="502cb-224">Filter recurring appointments and search for a string in the subject</span></span>](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [<span data-ttu-id="502cb-225">集計ビュー内のアイテムを検索して取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-225">Search and obtain items in an aggregated view</span></span>](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[<span data-ttu-id="502cb-226">セッション</span><span class="sxs-lookup"><span data-stu-id="502cb-226">Sessions</span></span>](sessions.md)

- [<span data-ttu-id="502cb-227">Outlook のインスタンスを取得し、サインインする</span><span class="sxs-lookup"><span data-stu-id="502cb-227">Get and sign in to an instance of Outlook</span></span>](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[<span data-ttu-id="502cb-228">ストア</span><span class="sxs-lookup"><span data-stu-id="502cb-228">Stores</span></span>](stores.md)

- [<span data-ttu-id="502cb-229">プロファイルのストアに関する情報を取得する</span><span class="sxs-lookup"><span data-stu-id="502cb-229">Get information about stores in a profile</span></span>](how-to-get-information-about-stores-in-a-profile.md)
- [<span data-ttu-id="502cb-230">ストアを追加または削除する</span><span class="sxs-lookup"><span data-stu-id="502cb-230">Add or remove a store</span></span>](how-to-add-or-remove-a-store.md)

[<span data-ttu-id="502cb-231">タスク</span><span class="sxs-lookup"><span data-stu-id="502cb-231">Tasks</span></span>](tasks.md)

- [<span data-ttu-id="502cb-232">作業アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-232">Create a task item</span></span>](how-to-create-a-task-item.md)
- [<span data-ttu-id="502cb-233">受信者にタスクを割り当てる</span><span class="sxs-lookup"><span data-stu-id="502cb-233">Assign a task to a recipient</span></span>](how-to-assign-a-task-to-a-recipient.md)
- [<span data-ttu-id="502cb-234">受信者に送信されたタスク依頼アイテムを表示する</span><span class="sxs-lookup"><span data-stu-id="502cb-234">Display the task request items sent to a recipient</span></span>](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [<span data-ttu-id="502cb-235">タスク依頼アイテムに返信する</span><span class="sxs-lookup"><span data-stu-id="502cb-235">Respond to a task request item</span></span>](how-to-respond-to-a-task-request-item.md)
- [<span data-ttu-id="502cb-236">定期タスクを作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-236">Create a recurring task</span></span>](how-to-create-a-recurring-task.md)
- [<span data-ttu-id="502cb-237">上司からのメール アイテムにフラグを設定する</span><span class="sxs-lookup"><span data-stu-id="502cb-237">Flag mail items from a manager for follow-up</span></span>](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[<span data-ttu-id="502cb-238">ビュー</span><span class="sxs-lookup"><span data-stu-id="502cb-238">Views</span></span>](views.md)

- [<span data-ttu-id="502cb-239">ビューを作成する</span><span class="sxs-lookup"><span data-stu-id="502cb-239">Create a view</span></span>](how-to-create-a-view.md)
- [<span data-ttu-id="502cb-240">ビューにフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="502cb-240">Add fields to a view</span></span>](how-to-add-fields-to-a-view.md)
- [<span data-ttu-id="502cb-241">表ビューのアイテムを列挙する</span><span class="sxs-lookup"><span data-stu-id="502cb-241">Enumerate items in a table view</span></span>](how-to-enumerate-items-in-a-table-view.md)



