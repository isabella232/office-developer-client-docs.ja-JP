---
title: 操作方法 (Outlook 2013 PIA リファレンス)
TOCTitle: How do I...
ms:assetid: ff647d52-bd32-4945-afa4-5b97d9a0d7dd
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612741(v=office.15)
ms:contentKeyID: 55119792
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f05f6e9199cd474a47d36ff92e255dea92a4d5cc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407556"
---
# <a name="how-do-i-outlook-2013-pia-reference"></a><span data-ttu-id="624b8-102">操作方法 (Outlook 2013 PIA リファレンス)</span><span class="sxs-lookup"><span data-stu-id="624b8-102">How do I... (Outlook 2013 PIA reference)</span></span>

<span data-ttu-id="624b8-103">このセクションにはタスク関連のトピックがまとめられています。ここでは、Outlook でよく使われる機能の実行方法を Visual Basic と C\# のコード例で示します。</span><span class="sxs-lookup"><span data-stu-id="624b8-103">This section contains procedural tasks topics and code examples in Visual Basic and C# that demonstrate how to perform some common tasks in Microsoft Outlook.</span></span>

<span data-ttu-id="624b8-104">これらのコード例を実行するには、Outlook 2010 と Visual Studio 2008、またはこれらの製品の新しいバージョンのインストールを完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="624b8-104">To run these code examples, you must have installed ol14short and visualstudio2008short, or a later version of these products.</span></span>

<span data-ttu-id="624b8-105">このセクションのコード例では、Visual Studio の Office Developer Tools がインストールされている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="624b8-105">The code examples in this section do not require that you have installed Office Developer Tools for Visual Studio.</span></span> <span data-ttu-id="624b8-106">ただし、ツールの使用についての詳細は [Office の開発を開始する](https://developer.microsoft.com/office/docs) ポータルを参照し、マネージ コードで書かれたいくつかの基本的な使い方に関するタスクについては 「[Outlook ソリューション](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017)」を参照していただけます。</span><span class="sxs-lookup"><span data-stu-id="624b8-106">However, you can refer to the [Getting started with Office development](https://developer.microsoft.com/office/docs) portal for information about using the tools, and refer to [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) for some basic how-to tasks written in managed code.</span></span>

<span data-ttu-id="624b8-107">このセクションのコード例には、初心者から中級者向けの例が含まれており、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493)』から抜粋した例も一部含まれています。</span><span class="sxs-lookup"><span data-stu-id="624b8-107">Code examples in this section range from the beginner to the intermediate levels, and some of them are adapted from the book [Programming Applications for Microsoft Office Outlook 2007http://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).</span></span>

<span data-ttu-id="624b8-108">タスクのアイデアやコード サンプルがございましたらぜひ Office 開発者向けドキュメント チームへお寄せください。</span><span class="sxs-lookup"><span data-stu-id="624b8-108">The Microsoft Office Developer Documentation team welcomes your task ideas and code samples! Topics tagged by the</span></span> <span data-ttu-id="624b8-109">お寄せいただいたコード サンプルを Outlook コンテンツで使用する場合は、お客様の署名とお客様の Web サイトへのリンクを記載してそれがお客様のものであることを案内します。</span><span class="sxs-lookup"><span data-stu-id="624b8-109">The Office Developer Documentation team welcomes your task ideas and code samples. If we use your code samples in Outlook content, we will recognize your work with a byline and a link to your Web site. For more information, contact us at docthis@microsoft.com.</span></span> <span data-ttu-id="624b8-110">詳細については、docthis@microsoft.com にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="624b8-110">For more information, contact us at docthis@microsoft.com.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="624b8-111">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="624b8-111">In this section</span></span> 

[<span data-ttu-id="624b8-112">アカウント</span><span class="sxs-lookup"><span data-stu-id="624b8-112">Accounts</span></span>](accounts.md)

- [<span data-ttu-id="624b8-113">アカウント情報を取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-113">Get account information</span></span>](how-to-get-account-information.md)
- [<span data-ttu-id="624b8-114">現在のフォルダーに基づいて特定のアカウントの送信可能なアイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-114">Create a Sendable Item for a Specific Account Based on the Current Folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [<span data-ttu-id="624b8-115">フォルダーのアカウントを取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-115">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md)
- [<span data-ttu-id="624b8-116">複数のアカウントの情報を取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-116">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md)
- <span data-ttu-id="624b8-117">[Hotmail アカウントを使用してメール アイテムを送信する](how-to-send-a-mail-item-by-using-a-hotmail-account.md)</span><span class="sxs-lookup"><span data-stu-id="624b8-117">Uses the [SendUsingAccount](how-to-send-a-mail-item-by-using-a-hotmail-account.md) property to send a mail item by using a Windows Live Hotmail account.</span></span>

[<span data-ttu-id="624b8-118">アドイン管理</span><span class="sxs-lookup"><span data-stu-id="624b8-118">Add-in Administration</span></span>](add-in-administration.md)

- [<span data-ttu-id="624b8-119">コンピューター上で Outlook がクイック実行アプリケーションかどうかを確認する</span><span class="sxs-lookup"><span data-stu-id="624b8-119">Determine whether Outlook is a Click-to-Run application on a computer</span></span>](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[<span data-ttu-id="624b8-120">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="624b8-120">Address Book</span></span>](address-book.md)

- <span data-ttu-id="624b8-121">[Contacts フォルダーに対応するアドレス帳を [名前の選択] ダイアログ ボックスに表示する](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)</span><span class="sxs-lookup"><span data-stu-id="624b8-121">[Display in the Select Names dialog box the address book corresponding to a Contacts folder](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)</span></span>
- [<span data-ttu-id="624b8-122">ストアのグローバル アドレス一覧またはアドレス一覧のセットを取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-122">Get the Global Address List or a set of address lists for a store</span></span>](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [<span data-ttu-id="624b8-123">グローバル アドレス一覧のエントリを列挙する</span><span class="sxs-lookup"><span data-stu-id="624b8-123">How to: Enumerate the Entries in the Global Address List</span></span>](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [<span data-ttu-id="624b8-124">プロファイルのアドレス一覧を表示する</span><span class="sxs-lookup"><span data-stu-id="624b8-124">Display the address lists for a profile</span></span>](how-to-display-the-address-lists-for-a-profile.md)

[<span data-ttu-id="624b8-125">予定</span><span class="sxs-lookup"><span data-stu-id="624b8-125">Appointments</span></span>](appointments.md)

- <span data-ttu-id="624b8-126">[終日イベントの予定を作成する](how-to-create-an-appointment-that-is-an-all-day-event.md)</span><span class="sxs-lookup"><span data-stu-id="624b8-126">Uses the [AllDayEvent](how-to-create-an-appointment-that-is-an-all-day-event.md) property to create an appointment that is an all-day event.</span></span>
- [<span data-ttu-id="624b8-127">太平洋タイム ゾーンで開始して東部タイム ゾーンで終了する予定を作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-127">How to: Create an Appointment That Starts in the Pacific Time Zone and Ends in the Eastern Time Zone</span></span>](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- <span data-ttu-id="624b8-128">[予定アイテムに異なる受信者の種類を指定する](how-to-specify-different-recipient-types-for-an-appointment-item.md)</span><span class="sxs-lookup"><span data-stu-id="624b8-128">Uses the [OlMeetingRecipientType](how-to-specify-different-recipient-types-for-an-appointment-item.md) enumeration to specify different recipient types for an appointment item.</span></span>
- [<span data-ttu-id="624b8-129">既定の定期的なパターンを使用して、定期的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-129">Creates a recurring appointment by using the default recurrence pattern.</span></span>](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [<span data-ttu-id="624b8-130">週単位パターンの定期的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-130">Create a recurring appointment that has a weekly pattern</span></span>](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [<span data-ttu-id="624b8-131">YearNth パターンの年単位の定期的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-131">Create an annual recurring appointment that uses a YearNth pattern</span></span>](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [<span data-ttu-id="624b8-132">定期的な一連の予定から特定の予定を検索する</span><span class="sxs-lookup"><span data-stu-id="624b8-132">Find a specific appointment in a recurring appointment series</span></span>](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="624b8-133">定期的な一連の予定に例外的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-133">Create an exception appointment in a recurring appointment series</span></span>](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="624b8-134">予定アイテムのリマインダーを作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-134">Create a reminder for an appointment item</span></span>](how-to-create-a-reminder-for-an-appointment-item.md)
- [<span data-ttu-id="624b8-135">予定の XML データを Outlook の予定オブジェクトにインポートする</span><span class="sxs-lookup"><span data-stu-id="624b8-135">Import Appointment XML Data into Outlook Appointment Objects</span></span>](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[<span data-ttu-id="624b8-136">添付ファイル</span><span class="sxs-lookup"><span data-stu-id="624b8-136">Attachments</span></span>](attachments.md)

- [<span data-ttu-id="624b8-137">メール アイテムにファイルを添付する</span><span class="sxs-lookup"><span data-stu-id="624b8-137">Attach a File to a Mail Item</span></span>](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [<span data-ttu-id="624b8-138">Outlook の連絡先アイテムを電子メール メッセージに添付する</span><span class="sxs-lookup"><span data-stu-id="624b8-138">Attach an Outlook Contact Item to an Email Message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [<span data-ttu-id="624b8-139">Outlook 電子メール メッセージの添付ファイルのサイズを制限する</span><span class="sxs-lookup"><span data-stu-id="624b8-139">Limit the Size of an Attachment to an Outlook Email Message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [<span data-ttu-id="624b8-140">Outlook 電子メール メッセージの添付ファイルを変更する</span><span class="sxs-lookup"><span data-stu-id="624b8-140">Modify an Attachment of an Outlook Email Message</span></span>](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [<span data-ttu-id="624b8-141">プログラムでメッセージからセキュリティ レベル 2 の添付ファイルを削除してディスクに保存する</span><span class="sxs-lookup"><span data-stu-id="624b8-141">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[<span data-ttu-id="624b8-142">Calendar</span><span class="sxs-lookup"><span data-stu-id="624b8-142">Calendar</span></span>](calendar.md)

- [<span data-ttu-id="624b8-143">予定表で指定した期間内の空き時間スケジュールを共有する</span><span class="sxs-lookup"><span data-stu-id="624b8-143">Share Free/Busy schedule within a specified period in a calendar</span></span>](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [<span data-ttu-id="624b8-144">電子メールで予定表情報を共有する</span><span class="sxs-lookup"><span data-stu-id="624b8-144">Share calendar information through email</span></span>](how-to-share-calendar-information-through-e-mail.md)
- [<span data-ttu-id="624b8-145">受信者の共有の予定表を表示する</span><span class="sxs-lookup"><span data-stu-id="624b8-145">Display a shared calendar of a recipient</span></span>](how-to-display-a-shared-calendar-of-a-recipient.md)
- [<span data-ttu-id="624b8-146">予定表をディスクに保存する</span><span class="sxs-lookup"><span data-stu-id="624b8-146">Save a calendar to disk</span></span>](how-to-save-a-calendar-to-disk.md)
- [<span data-ttu-id="624b8-147">iCalendar ファイルを開いて内容を表示する</span><span class="sxs-lookup"><span data-stu-id="624b8-147">Open and display the contents of an iCalendar file</span></span>](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[<span data-ttu-id="624b8-148">色の分類項目</span><span class="sxs-lookup"><span data-stu-id="624b8-148">Color Categories</span></span>](color-categories.md)

- [<span data-ttu-id="624b8-149">分類項目を列挙および追加する</span><span class="sxs-lookup"><span data-stu-id="624b8-149">Enumerate and add categories</span></span>](how-to-enumerate-and-add-categories.md)
- [<span data-ttu-id="624b8-150">分類項目をアイテムに割り当てる</span><span class="sxs-lookup"><span data-stu-id="624b8-150">Assign categories to an item</span></span>](how-to-assign-categories-to-an-item.md)

[<span data-ttu-id="624b8-151">連絡先</span><span class="sxs-lookup"><span data-stu-id="624b8-151">Contacts</span></span>](contacts.md)

- [<span data-ttu-id="624b8-152">連絡先アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-152">Create a Contact item</span></span>](how-to-create-a-contact-item.md)
- [<span data-ttu-id="624b8-153">カスタムの連絡先アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-153">Create a custom Contact item</span></span>](how-to-create-a-custom-contact-item.md)
- [<span data-ttu-id="624b8-154">vCard ファイルから連絡先アイテムを作成し、フォルダーにアイテムを保存する</span><span class="sxs-lookup"><span data-stu-id="624b8-154">Create a Contact item from a vCard file and save the item in a folder</span></span>](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[<span data-ttu-id="624b8-155">会話</span><span class="sxs-lookup"><span data-stu-id="624b8-155">Conversations</span></span>](conversations.md)

- [<span data-ttu-id="624b8-156">スレッド内のアイテムを取得して表示する</span><span class="sxs-lookup"><span data-stu-id="624b8-156">Get and display items in a conversation</span></span>](how-to-get-and-display-items-in-a-conversation.md)
- [<span data-ttu-id="624b8-157">選択されたスレッドを取得して列挙する</span><span class="sxs-lookup"><span data-stu-id="624b8-157">Get and enumerate selected conversations</span></span>](how-to-get-and-enumerate-selected-conversations.md)

[<span data-ttu-id="624b8-158">電子名刺</span><span class="sxs-lookup"><span data-stu-id="624b8-158">Electronic Business Cards</span></span>](electronic-business-cards.md)

- [<span data-ttu-id="624b8-159">電子名刺のレイアウトを変更する</span><span class="sxs-lookup"><span data-stu-id="624b8-159">Modify the layout of an electronic business card</span></span>](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [<span data-ttu-id="624b8-160">電子名刺付きのメール アイテムを送信する</span><span class="sxs-lookup"><span data-stu-id="624b8-160">Send a mail item with an electronic business card</span></span>](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[<span data-ttu-id="624b8-161">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="624b8-161">Exchange Users</span></span>](exchange-users.md)

- [<span data-ttu-id="624b8-162">現在のユーザーの情報を取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-162">Get information about the signed in user.</span></span>](how-to-get-information-about-the-current-user.md)
- [<span data-ttu-id="624b8-163">現在のユーザーがメンバーになっているすべての配布リストについての情報を取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-163">Get information about all distribution lists of which the current user is a member</span></span>](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [<span data-ttu-id="624b8-164">配布リストを作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-164">Create a list:</span></span>](how-to-create-a-distribution-list.md)
- [<span data-ttu-id="624b8-165">Exchange 配布リストのメンバーを取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-165">Get members of an Exchange distribution list</span></span>](how-to-get-members-of-an-exchange-distribution-list.md)
- [<span data-ttu-id="624b8-166">現在のユーザーの上司の情報を取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-166">Get information about the current user's manager</span></span>](how-to-get-information-about-the-current-user-s-manager.md)
- [<span data-ttu-id="624b8-167">Exchange ユーザーの上司の空き時間情報を取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-167">Get availability information for an Exchange user's manager</span></span>](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [<span data-ttu-id="624b8-168">会議出席依頼に対する上司からの返信を確認する</span><span class="sxs-lookup"><span data-stu-id="624b8-168">Check a manager's response to a meeting request</span></span>](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [<span data-ttu-id="624b8-169">現在のユーザーの上司の直属部下についての情報を取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-169">Get information about direct reports of the current user's manager</span></span>](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[<span data-ttu-id="624b8-170">フォルダー</span><span class="sxs-lookup"><span data-stu-id="624b8-170">Folders</span></span>](folders.md)

- [<span data-ttu-id="624b8-171">フォルダー一覧にフォルダーを追加する</span><span class="sxs-lookup"><span data-stu-id="624b8-171">Add a folder to the folder list</span></span>](how-to-add-a-folder-to-the-folder-list.md)
- [<span data-ttu-id="624b8-172">フォルダーを列挙する</span><span class="sxs-lookup"><span data-stu-id="624b8-172">Enumerate folders</span></span>](how-to-enumerate-folders.md)
- [<span data-ttu-id="624b8-173">既定のフォルダーを取得して、そのサブフォルダーを列挙する</span><span class="sxs-lookup"><span data-stu-id="624b8-173">Get a default folder and enumerate its subfolders</span></span>](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [<span data-ttu-id="624b8-174">フォルダーのパスに基づいてフォルダーを取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-174">Get a folder based on its folder path</span></span>](how-to-get-a-folder-based-on-its-folder-path.md)
- [<span data-ttu-id="624b8-175">フォルダーを選択してフォルダーの情報を表示する</span><span class="sxs-lookup"><span data-stu-id="624b8-175">Select a folder and display folder information</span></span>](how-to-select-a-folder-and-display-folder-information.md)
- [<span data-ttu-id="624b8-176">フォルダーの既定のメッセージ クラスを取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-176">Get the default message class of a folder</span></span>](how-to-get-the-default-message-class-of-a-folder.md)
- [<span data-ttu-id="624b8-177">非表示メッセージとしてフォルダーに格納されているソリューション固有のデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="624b8-177">Access solution-specific data stored as a hidden message in a folder</span></span>](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [<span data-ttu-id="624b8-178">フォルダー レベルのクエリでカスタム アイテム プロパティが確実にサポートされるようにする</span><span class="sxs-lookup"><span data-stu-id="624b8-178">Ensure that custom item properties are supported in folder-level queries</span></span>](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[<span data-ttu-id="624b8-179">Outlook アイテム全般</span><span class="sxs-lookup"><span data-stu-id="624b8-179">General Outlook Items</span></span>](general-outlook-items.md)

- [<span data-ttu-id="624b8-180">ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする</span><span class="sxs-lookup"><span data-stu-id="624b8-180">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="624b8-181">アクティブ エクスプローラーで選択した項目を表示する</span><span class="sxs-lookup"><span data-stu-id="624b8-181">Display selected items in the active Explorer</span></span>](how-to-display-selected-items-in-the-active-explorer.md)

[<span data-ttu-id="624b8-182">グループ共有</span><span class="sxs-lookup"><span data-stu-id="624b8-182">Group Sharing</span></span>](group-sharing.md)

- [<span data-ttu-id="624b8-183">RSS フィードを購読する</span><span class="sxs-lookup"><span data-stu-id="624b8-183">Subscribe to an RSS feed</span></span>](how-to-subscribe-to-an-rss-feed.md)
- [<span data-ttu-id="624b8-184">Outlook と SharePoint のフォルダーを同期させる</span><span class="sxs-lookup"><span data-stu-id="624b8-184">How to: Synchronize Outlook with a SharePoint Folder</span></span>](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[<span data-ttu-id="624b8-185">メール</span><span class="sxs-lookup"><span data-stu-id="624b8-185">Mail</span></span>](mail.md)

- [<span data-ttu-id="624b8-186">メッセージ テンプレートを使用してメール アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-186">Create a mail item by using a message template</span></span>](how-to-create-a-mail-item-by-using-a-message-template.md)
- [<span data-ttu-id="624b8-187">メール アイテムを作成し、レポートを添付して、ユーザーの上司にメール アイテムを送信する</span><span class="sxs-lookup"><span data-stu-id="624b8-187">Create a mail item, attach a report, and send the mail item to the user's manager</span></span>](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [<span data-ttu-id="624b8-188">アカウントの SMTP アドレスを指定して電子メールを送信する</span><span class="sxs-lookup"><span data-stu-id="624b8-188">Send an E-mail Given the SMTP Address of an Account</span></span>](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [<span data-ttu-id="624b8-189">メール アイテムに投票オプションを追加する</span><span class="sxs-lookup"><span data-stu-id="624b8-189">Add voting options to a mail item</span></span>](how-to-add-voting-options-to-a-mail-item.md)
- [<span data-ttu-id="624b8-190">メール アイテムへの返信として行うカスタム アクションを追加する</span><span class="sxs-lookup"><span data-stu-id="624b8-190">Add a custom action as a response to a mail item</span></span>](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [<span data-ttu-id="624b8-191">メール アイテムの差出人の SMTP アドレスを取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-191">Get the SMTP address of the sender of a mail item</span></span>](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [<span data-ttu-id="624b8-192">メール アイテムのさまざまな受信者の種類を指定する</span><span class="sxs-lookup"><span data-stu-id="624b8-192">Specify different recipient types for a mail item</span></span>](how-to-specify-different-recipient-types-for-a-mail-item.md)

[<span data-ttu-id="624b8-193">会議出席依頼</span><span class="sxs-lookup"><span data-stu-id="624b8-193">Meeting requests</span></span>](meeting-requests.md)

- [<span data-ttu-id="624b8-194">会議出席依頼を作成し、受信者を追加して、場所を指定する</span><span class="sxs-lookup"><span data-stu-id="624b8-194">Create a meeting request, add recipients, and specify a location</span></span>](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [<span data-ttu-id="624b8-195">会議の開催者を取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-195">Get the organizer of a meeting</span></span>](how-to-get-the-organizer-of-a-meeting.md)
- [<span data-ttu-id="624b8-196">会議出席依頼へのすべての返信を調べる</span><span class="sxs-lookup"><span data-stu-id="624b8-196">Check all responses to a meeting request</span></span>](how-to-check-all-responses-to-a-meeting-request.md)
- [<span data-ttu-id="624b8-197">会議出席依頼に関連付けられている予定アイテムを検索する</span><span class="sxs-lookup"><span data-stu-id="624b8-197">Find the appointment item associated with a meeting request</span></span>](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [<span data-ttu-id="624b8-198">会議出席依頼を自動的に承諾する</span><span class="sxs-lookup"><span data-stu-id="624b8-198">Automatically accept a meeting request</span></span>](how-to-automatically-accept-a-meeting-request.md)
- [<span data-ttu-id="624b8-199">会議出席依頼への返信をユーザーに求める</span><span class="sxs-lookup"><span data-stu-id="624b8-199">Prompt a user to respond to a meeting request</span></span>](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[<span data-ttu-id="624b8-200">受信者</span><span class="sxs-lookup"><span data-stu-id="624b8-200">Recipients</span></span>](recipients.md)

- <span data-ttu-id="624b8-201">[[名前の選択] ダイアログ ボックスを表示して受信者を解決する](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)</span><span class="sxs-lookup"><span data-stu-id="624b8-201">[Display the Select Names dialog box to resolve recipients](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)</span></span>
- <span data-ttu-id="624b8-202">[[名前の選択] ダイアログ ボックスを使用して、受信者を取得し、予定に割り当てる](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)</span><span class="sxs-lookup"><span data-stu-id="624b8-202">[Use the Select Names dialog box to obtain and assign recipients to an appointment](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)</span></span>
- [<span data-ttu-id="624b8-203">受信者のメール アドレス</span><span class="sxs-lookup"><span data-stu-id="624b8-203">Get the email address of a recipient</span></span>](how-to-get-the-e-mail-address-of-a-recipient.md)

[<span data-ttu-id="624b8-204">ルール</span><span class="sxs-lookup"><span data-stu-id="624b8-204">Rules</span></span>](rules.md)

- [<span data-ttu-id="624b8-205">上司からのメール アイテムを分類して確認のフラグを設定する</span><span class="sxs-lookup"><span data-stu-id="624b8-205">Create a rule to file mail items from a manager and flag them for follow-up</span></span>](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [<span data-ttu-id="624b8-206">ルールを直ちに実行する</span><span class="sxs-lookup"><span data-stu-id="624b8-206">Execute a rule instantly</span></span>](how-to-execute-a-rule-instantly.md)
- [<span data-ttu-id="624b8-207">ローカル コンピューターでルールを実行する</span><span class="sxs-lookup"><span data-stu-id="624b8-207">Execute a rule on a local computer</span></span>](how-to-execute-a-rule-on-a-local-computer.md)
- [<span data-ttu-id="624b8-208">件名内の複数の単語に基づいてメール アイテムに分類項目を割り当てるルールを作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-208">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[<span data-ttu-id="624b8-209">Outlook のイベントを使用するサンプル タスク</span><span class="sxs-lookup"><span data-stu-id="624b8-209">Sample Tasks Using Outlook Events</span></span>](sample-tasks-using-outlook-events.md)

- [<span data-ttu-id="624b8-210">インスペクターのラッパーを実装し、インスペクターごとにアイテム レベルのイベントを追跡する</span><span class="sxs-lookup"><span data-stu-id="624b8-210">Implement a Wrapper for Inspectors and Track Item-Level Events in Each Inspector</span></span>](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[<span data-ttu-id="624b8-211">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="624b8-211">Search and Filter</span></span>](search-and-filter.md)

- [<span data-ttu-id="624b8-212">フォルダーのアイテムをフィルター処理して効率よく列挙する</span><span class="sxs-lookup"><span data-stu-id="624b8-212">Filter and efficiently enumerate items in a folder</span></span>](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="624b8-213">SetColumns を使用してフォルダーのアイテムを効率よく列挙する</span><span class="sxs-lookup"><span data-stu-id="624b8-213">Use SetColumns to efficiently enumerate items in a folder</span></span>](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="624b8-214">配列を使用してフォルダーのアイテムを効率よく列挙する</span><span class="sxs-lookup"><span data-stu-id="624b8-214">Use arrays to efficiently enumerate items in a folder</span></span>](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="624b8-215">最終変更時刻に基づいて受信トレイ内のアイテムを列挙する</span><span class="sxs-lookup"><span data-stu-id="624b8-215">Enumerate items in the Inbox based on the last modification time</span></span>](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [<span data-ttu-id="624b8-216">先月変更された受信トレイ アイテムをフィルター処理して表示する</span><span class="sxs-lookup"><span data-stu-id="624b8-216">Filter and display Inbox items modified in the last month</span></span>](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [<span data-ttu-id="624b8-217">フォルダー内のアイテムの列挙時に複数値プロパティをフィルター処理して表示する</span><span class="sxs-lookup"><span data-stu-id="624b8-217">Filter and display multivalued properties when enumerating items in a folder</span></span>](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="624b8-218">フォルダー内のアイテムの列挙時に、計算済みのプロパティをフィルター処理して表示する</span><span class="sxs-lookup"><span data-stu-id="624b8-218">This example shows how to filter and display computed properties when enumerating items in a folder.</span></span>](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="624b8-219">フォルダー内の非表示のアイテムを列挙する</span><span class="sxs-lookup"><span data-stu-id="624b8-219">Enumerate hidden items in a folder</span></span>](how-to-enumerate-hidden-items-in-a-folder.md)
- [<span data-ttu-id="624b8-220">クイック検索を使用して、すべてのフォルダーとすべてのストアから件名の特定の語句を検索する</span><span class="sxs-lookup"><span data-stu-id="624b8-220">Use instant search to search all folders and all stores for a phrase in the subject</span></span>](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [<span data-ttu-id="624b8-221">フォルダー内のアイテムの本文で語句を検索する</span><span class="sxs-lookup"><span data-stu-id="624b8-221">Search for a phrase in the body of items in a folder</span></span>](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [<span data-ttu-id="624b8-222">フォルダー内のアイテムの添付ファイルで完全に一致する語句を検索する</span><span class="sxs-lookup"><span data-stu-id="624b8-222">Search attachments of items in a folder for an exact phrase</span></span>](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [<span data-ttu-id="624b8-223">時間範囲内の予定を検索、取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-223">Search and obtain appointments in a time range</span></span>](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [<span data-ttu-id="624b8-224">定期的な予定でフィルター処理した後、件名の文字列を検索する</span><span class="sxs-lookup"><span data-stu-id="624b8-224">Filter recurring appointments and search for a string in the subject</span></span>](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [<span data-ttu-id="624b8-225">集計ビュー内のアイテムを検索して取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-225">Search and Obtain Items in an Aggregated View</span></span>](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[<span data-ttu-id="624b8-226">セッション</span><span class="sxs-lookup"><span data-stu-id="624b8-226">Sessions</span></span>](sessions.md)

- [<span data-ttu-id="624b8-227">Outlook のインスタンスを取得し、サインインする</span><span class="sxs-lookup"><span data-stu-id="624b8-227">Get and sign in to an instance of Outlook</span></span>](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[<span data-ttu-id="624b8-228">ストア</span><span class="sxs-lookup"><span data-stu-id="624b8-228">Stores</span></span>](stores.md)

- [<span data-ttu-id="624b8-229">プロファイルのストアに関する情報を取得する</span><span class="sxs-lookup"><span data-stu-id="624b8-229">Get information about stores in a profile</span></span>](how-to-get-information-about-stores-in-a-profile.md)
- [<span data-ttu-id="624b8-230">ストアを追加または削除する</span><span class="sxs-lookup"><span data-stu-id="624b8-230">Add or remove a store</span></span>](how-to-add-or-remove-a-store.md)

[<span data-ttu-id="624b8-231">タスク</span><span class="sxs-lookup"><span data-stu-id="624b8-231">Tasks</span></span>](tasks.md)

- [<span data-ttu-id="624b8-232">作業アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-232">Create a new task</span></span>](how-to-create-a-task-item.md)
- [<span data-ttu-id="624b8-233">受信者にタスクを割り当てる</span><span class="sxs-lookup"><span data-stu-id="624b8-233">Assign a task to a recipient</span></span>](how-to-assign-a-task-to-a-recipient.md)
- [<span data-ttu-id="624b8-234">受信者に送信されたタスク依頼アイテムを表示する</span><span class="sxs-lookup"><span data-stu-id="624b8-234">Display the task request items sent to a recipient</span></span>](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [<span data-ttu-id="624b8-235">タスク依頼アイテムに返信する</span><span class="sxs-lookup"><span data-stu-id="624b8-235">Respond to a task request item</span></span>](how-to-respond-to-a-task-request-item.md)
- [<span data-ttu-id="624b8-236">定期タスクを作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-236">Create a recurring task</span></span>](how-to-create-a-recurring-task.md)
- [<span data-ttu-id="624b8-237">上司からのメール アイテムにフラグを設定する</span><span class="sxs-lookup"><span data-stu-id="624b8-237">Flag mail items from a manager for follow-up</span></span>](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[<span data-ttu-id="624b8-238">ビュー</span><span class="sxs-lookup"><span data-stu-id="624b8-238">Views</span></span>](views.md)

- [<span data-ttu-id="624b8-239">ビューを作成する</span><span class="sxs-lookup"><span data-stu-id="624b8-239">Create a view</span></span>](how-to-create-a-view.md)
- [<span data-ttu-id="624b8-240">ビューにフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="624b8-240">Add fields to a view</span></span>](how-to-add-fields-to-a-view.md)
- [<span data-ttu-id="624b8-241">表ビューのアイテムを列挙する</span><span class="sxs-lookup"><span data-stu-id="624b8-241">Enumerate items in a table view</span></span>](how-to-enumerate-items-in-a-table-view.md)



