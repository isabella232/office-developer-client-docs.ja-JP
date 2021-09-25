---
title: フォルダー
TOCTitle: Folders
ms:assetid: b72b5705-d77a-4cad-873d-457b9fb6553e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184634(v=office.15)
ms:contentKeyID: 55119856
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9605ecfc70bb1cc583d81f3287a625d0fc4e3a7e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590850"
---
# <a name="folders"></a>フォルダー

This section provides sample tasks that involve folders. [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) objects represent the folder hierarchy where Microsoft Outlook items are stored. Examples of folders include the Calendar, Mail, and Deleted Items folders. In the Outlook Primary Interop Assembly (PIA), members of the **Folder** object are exposed as members of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.

## <a name="in-this-section"></a>このセクションの内容

|トピック|説明|
|:----|:----------|
|[フォルダー一覧にフォルダーを追加する](how-to-add-a-folder-to-the-folder-list.md) |[Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) メソッドを使用して、Outlook のフォルダー一覧にフォルダーを追加します。|
|[フォルダーを列挙する](how-to-enumerate-folders.md)  |フォルダーのコレクションに対して順に処理を行い、フォルダーを列挙します。|
|[既定のフォルダーを取得して、そのサブフォルダーを列挙する](how-to-get-a-default-folder-and-enumerate-its-subfolders.md) |ユーザーの既定のストアで既定のフォルダーを取得し、そのサブフォルダーを列挙します。|
|[フォルダーのパスに基づいてフォルダーを取得する](how-to-get-a-folder-based-on-its-folder-path.md)  |フォルダーのパスを取得することで、関連するフォルダーを取得します。|
|[フォルダーを選択してフォルダーの情報を表示する](how-to-select-a-folder-and-display-folder-information.md)  |指定のフォルダー一覧からユーザーが選択するフォルダーについての情報をプログラムで表示します。|
|[フォルダーの既定のメッセージ クラスを取得する](how-to-get-the-default-message-class-of-a-folder.md)  |[DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) プロパティを使用して、フォルダーの既定のメッセージ クラスを取得します。|
|[非表示メッセージとしてフォルダーに格納されているソリューション固有のデータにアクセスする](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)  |[StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) オブジェクトを使用して、特定のメッセージ クラスの非表示メッセージとしてフォルダーに格納されているデータを取得します。|
|[フォルダー レベルのクエリでカスタム アイテム プロパティが確実にサポートされるようにする](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md) |あるアイテム型にカスタム プロパティを追加した場合に、フォルダーにもそのプロパティを追加して、フォルダー レベルでそのカスタム プロパティに対するクエリを実行できるようにする方法を示します。|

## <a name="see-also"></a>関連項目

- [予定表](calendar.md)
- [連絡先](contacts.md)
- [メール](mail.md)
- [操作方法 (Outlook 2013 PIA リファレンス)](how-do-i-outlook-2013-pia-reference.md)

