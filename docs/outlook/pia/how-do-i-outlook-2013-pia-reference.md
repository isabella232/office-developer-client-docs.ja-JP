---
title: 操作方法 (Outlook 2013 PIA リファレンス)
TOCTitle: How do I...
ms:assetid: ff647d52-bd32-4945-afa4-5b97d9a0d7dd
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612741(v=office.15)
ms:contentKeyID: 55119792
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 160e6fe9607ec2892461c6109d4ff4264f73735e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629425"
---
# <a name="how-do-i-outlook-2013-pia-reference"></a>操作方法 (Outlook 2013 PIA リファレンス)

このセクションにはタスク関連のトピックがまとめられています。ここでは、Outlook でよく使われる機能の実行方法を Visual Basic と C\# のコード例で示します。

これらのコード例を実行するには、Outlook 2010 と Visual Studio 2008、またはこれらの製品の新しいバージョンのインストールを完了している必要があります。

このセクションのコード例では、Visual Studio の Office Developer Tools がインストールされている必要はありません。 ただし、ツールの使用についての詳細は [Office の開発を開始する](https://developer.microsoft.com/office/docs) ポータルを参照し、マネージ コードで書かれたいくつかの基本的な使い方に関するタスクについては 「[Outlook ソリューション](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017)」を参照していただけます。

このセクションのコード例には、初心者から中級者向けの例が含まれており、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493)』から抜粋した例も一部含まれています。

タスクのアイデアやコード サンプルがございましたらぜひ Office 開発者向けドキュメント チームへお寄せください。 お寄せいただいたコード サンプルを Outlook コンテンツで使用する場合は、お客様の署名とお客様の Web サイトへのリンクを記載してそれがお客様のものであることを案内します。 詳細については、docthis@microsoft.com にお問い合わせください。

## <a name="in-this-section"></a>このセクションの内容 

[アカウント](accounts.md)

- [アカウント情報を取得する](how-to-get-account-information.md)
- [現在のフォルダーに基づいて特定のアカウントの送信可能なアイテムを作成する](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [フォルダーのアカウントを取得する](how-to-get-the-account-for-a-folder.md)
- [複数のアカウントの情報を取得する](how-to-get-information-about-multiple-accounts.md)
- [Hotmail アカウントを使用してメール アイテムを送信する](how-to-send-a-mail-item-by-using-a-hotmail-account.md)

[アドイン管理](add-in-administration.md)

- [コンピューター上で Outlook がクイック実行アプリケーションかどうかを確認する](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[アドレス帳](address-book.md)

- [Contacts フォルダーに対応するアドレス帳を [名前の選択] ダイアログ ボックスに表示する](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)
- [ストアのグローバル アドレス一覧またはアドレス一覧のセットを取得する](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [グローバル アドレス一覧のエントリを列挙する](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [プロファイルのアドレス一覧を表示する](how-to-display-the-address-lists-for-a-profile.md)

[予定](appointments.md)

- [終日イベントの予定を作成する](how-to-create-an-appointment-that-is-an-all-day-event.md)
- [太平洋タイム ゾーンで開始して東部タイム ゾーンで終了する予定を作成する](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- [予定アイテムに異なる受信者の種類を指定する](how-to-specify-different-recipient-types-for-an-appointment-item.md)
- [既定の定期的なパターンを使用して、定期的な予定を作成する](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [週単位パターンの定期的な予定を作成する](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [YearNth パターンの年単位の定期的な予定を作成する](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [定期的な一連の予定から特定の予定を検索する](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [定期的な一連の予定に例外的な予定を作成する](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [予定アイテムのリマインダーを作成する](how-to-create-a-reminder-for-an-appointment-item.md)
- [予定の XML データを Outlook の予定オブジェクトにインポートする](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[添付ファイル](attachments.md)

- [メール アイテムにファイルを添付する](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [Outlook の連絡先アイテムを電子メール メッセージに添付する](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [Outlook 電子メール メッセージの添付ファイルのサイズを制限する](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [Outlook 電子メール メッセージの添付ファイルを変更する](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [プログラムでメッセージからセキュリティ レベル 2 の添付ファイルを削除してディスクに保存する](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[Calendar](calendar.md)

- [予定表で指定した期間内の空き時間スケジュールを共有する](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [電子メールで予定表情報を共有する](how-to-share-calendar-information-through-e-mail.md)
- [受信者の共有の予定表を表示する](how-to-display-a-shared-calendar-of-a-recipient.md)
- [予定表をディスクに保存する](how-to-save-a-calendar-to-disk.md)
- [iCalendar ファイルを開いて内容を表示する](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[色の分類項目](color-categories.md)

- [分類項目を列挙および追加する](how-to-enumerate-and-add-categories.md)
- [分類項目をアイテムに割り当てる](how-to-assign-categories-to-an-item.md)

[連絡先](contacts.md)

- [連絡先アイテムを作成する](how-to-create-a-contact-item.md)
- [カスタムの連絡先アイテムを作成する](how-to-create-a-custom-contact-item.md)
- [vCard ファイルから連絡先アイテムを作成し、フォルダーにアイテムを保存する](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[会話](conversations.md)

- [スレッド内のアイテムを取得して表示する](how-to-get-and-display-items-in-a-conversation.md)
- [選択されたスレッドを取得して列挙する](how-to-get-and-enumerate-selected-conversations.md)

[電子名刺](electronic-business-cards.md)

- [電子名刺のレイアウトを変更する](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [電子名刺付きのメール アイテムを送信する](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[Exchange ユーザー](exchange-users.md)

- [現在のユーザーの情報を取得する](how-to-get-information-about-the-current-user.md)
- [現在のユーザーがメンバーになっているすべての配布リストについての情報を取得する](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [配布リストを作成する](how-to-create-a-distribution-list.md)
- [Exchange 配布リストのメンバーを取得する](how-to-get-members-of-an-exchange-distribution-list.md)
- [現在のユーザーの上司の情報を取得する](how-to-get-information-about-the-current-user-s-manager.md)
- [Exchange ユーザーの上司の空き時間情報を取得する](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [会議出席依頼に対する上司からの返信を確認する](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [現在のユーザーの上司の直属部下についての情報を取得する](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[フォルダー](folders.md)

- [フォルダー一覧にフォルダーを追加する](how-to-add-a-folder-to-the-folder-list.md)
- [フォルダーを列挙する](how-to-enumerate-folders.md)
- [既定のフォルダーを取得して、そのサブフォルダーを列挙する](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [フォルダーのパスに基づいてフォルダーを取得する](how-to-get-a-folder-based-on-its-folder-path.md)
- [フォルダーを選択してフォルダーの情報を表示する](how-to-select-a-folder-and-display-folder-information.md)
- [フォルダーの既定のメッセージ クラスを取得する](how-to-get-the-default-message-class-of-a-folder.md)
- [非表示メッセージとしてフォルダーに格納されているソリューション固有のデータにアクセスする](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [フォルダー レベルのクエリでカスタム アイテム プロパティが確実にサポートされるようにする](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[Outlook アイテム全般](general-outlook-items.md)

- [ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [アクティブ エクスプローラーで選択した項目を表示する](how-to-display-selected-items-in-the-active-explorer.md)

[グループ共有](group-sharing.md)

- [RSS フィードを購読する](how-to-subscribe-to-an-rss-feed.md)
- [Outlook と SharePoint のフォルダーを同期させる](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[メール](mail.md)

- [メッセージ テンプレートを使用してメール アイテムを作成する](how-to-create-a-mail-item-by-using-a-message-template.md)
- [メール アイテムを作成し、レポートを添付して、ユーザーの上司にメール アイテムを送信する](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [アカウントの SMTP アドレスを指定して電子メールを送信する](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [メール アイテムに投票オプションを追加する](how-to-add-voting-options-to-a-mail-item.md)
- [メール アイテムへの返信として行うカスタム アクションを追加する](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [メール アイテムの差出人の SMTP アドレスを取得する](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [メール アイテムのさまざまな受信者の種類を指定する](how-to-specify-different-recipient-types-for-a-mail-item.md)

[会議出席依頼](meeting-requests.md)

- [会議出席依頼を作成し、受信者を追加して、場所を指定する](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [会議の開催者を取得する](how-to-get-the-organizer-of-a-meeting.md)
- [会議出席依頼へのすべての返信を調べる](how-to-check-all-responses-to-a-meeting-request.md)
- [会議出席依頼に関連付けられている予定アイテムを検索する](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [会議出席依頼を自動的に承諾する](how-to-automatically-accept-a-meeting-request.md)
- [会議出席依頼への返信をユーザーに求める](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[受信者](recipients.md)

- [[名前の選択] ダイアログ ボックスを表示して受信者を解決する](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)
- [[名前の選択] ダイアログ ボックスを使用して、受信者を取得し、予定に割り当てる](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)
- [受信者のメール アドレス](how-to-get-the-e-mail-address-of-a-recipient.md)

[ルール](rules.md)

- [上司からのメール アイテムを分類して確認のフラグを設定する](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [ルールを直ちに実行する](how-to-execute-a-rule-instantly.md)
- [ローカル コンピューターでルールを実行する](how-to-execute-a-rule-on-a-local-computer.md)
- [件名内の複数の単語に基づいてメール アイテムに分類項目を割り当てるルールを作成する](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[Outlook のイベントを使用するサンプル タスク](sample-tasks-using-outlook-events.md)

- [インスペクターのラッパーを実装し、インスペクターごとにアイテム レベルのイベントを追跡する](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[検索とフィルター](search-and-filter.md)

- [フォルダーのアイテムをフィルター処理して効率よく列挙する](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [SetColumns を使用してフォルダーのアイテムを効率よく列挙する](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [配列を使用してフォルダーのアイテムを効率よく列挙する](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [最終変更時刻に基づいて受信トレイ内のアイテムを列挙する](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [先月変更された受信トレイ アイテムをフィルター処理して表示する](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [フォルダー内のアイテムの列挙時に複数値プロパティをフィルター処理して表示する](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [フォルダー内のアイテムの列挙時に、計算済みのプロパティをフィルター処理して表示する](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [フォルダー内の非表示のアイテムを列挙する](how-to-enumerate-hidden-items-in-a-folder.md)
- [クイック検索を使用して、すべてのフォルダーとすべてのストアから件名の特定の語句を検索する](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [フォルダー内のアイテムの本文で語句を検索する](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [フォルダー内のアイテムの添付ファイルで完全に一致する語句を検索する](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [時間範囲内の予定を検索、取得する](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [定期的な予定でフィルター処理した後、件名の文字列を検索する](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [集計ビュー内のアイテムを検索して取得する](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[セッション](sessions.md)

- [Outlook のインスタンスを取得し、サインインする](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[ストア](stores.md)

- [プロファイルのストアに関する情報を取得する](how-to-get-information-about-stores-in-a-profile.md)
- [ストアを追加または削除する](how-to-add-or-remove-a-store.md)

[タスク](tasks.md)

- [作業アイテムを作成する](how-to-create-a-task-item.md)
- [受信者にタスクを割り当てる](how-to-assign-a-task-to-a-recipient.md)
- [受信者に送信されたタスク依頼アイテムを表示する](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [タスク依頼アイテムに返信する](how-to-respond-to-a-task-request-item.md)
- [定期タスクを作成する](how-to-create-a-recurring-task.md)
- [上司からのメール アイテムにフラグを設定する](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[ビュー](views.md)

- [ビューを作成する](how-to-create-a-view.md)
- [ビューにフィールドを追加する](how-to-add-fields-to-a-view.md)
- [表ビューのアイテムを列挙する](how-to-enumerate-items-in-a-table-view.md)



