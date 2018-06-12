---
title: エラー コード (OneNote 2013)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 390df5ce-e730-470d-b6e9-0de4a3e904f8
description: このトピックは、 OneNote 2013オブジェクト モデルでは、エラー コードを示します。
ms.openlocfilehash: 58c4d5d96182c49a1bc447c44763b9aaef1734ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799272"
---
# <a name="error-codes-onenote"></a>エラー コード (OneNote 2013)

このトピックは、 OneNote 2013オブジェクト モデルでは、エラー コードを示します。
  
|**HRESULT 型**|**値**|**Description**|
|:-----|:-----|:-----|
|hrMalformedXML  <br/> |0x80042000  <br/> |XML が整形式でないです。  <br/> |
|hrInvalidXML  <br/> |0x80042001  <br/> |XML が無効です。  <br/> |
|hrCreatingSection  <br/> |0x80042002  <br/> |セクションを作成できませんでした。  <br/> |
|hrOpeningSection  <br/> |0x80042003  <br/> |セクションを開くことができませんでした。  <br/> |
|hrSectionDoesNotExist  <br/> |0x80042004  <br/> |セクションが存在しません。  <br/> |
|hrPageDoesNotExist  <br/> |0x80042005  <br/> |ページは存在しません。  <br/> |
|hrFileDoesNotExist  <br/> |0x80042006  <br/> |ファイルが存在しません。  <br/> |
|hrInsertingImage  <br/> |0x80042007  <br/> |イメージを挿入できませんでした。  <br/> |
|hrInsertingInk  <br/> |0x80042008  <br/> |インクを挿入できませんでした。  <br/> |
|hrInsertingHtml  <br/> |0x80042009  <br/> |HTML を挿入できませんでした。  <br/> |
|hrNavigatingToPage  <br/> |0x8004200a  <br/> |ページを開くことができませんでした。  <br/> |
|hrSectionReadOnly  <br/> |0x8004200b  <br/> |セクションは、読み取り専用です。  <br/> |
|hrPageReadOnly  <br/> |0x8004200c  <br/> |ページは読み取り専用です。  <br/> |
|hrInsertingOutlineText  <br/> |0x8004200d  <br/> |アウトライン テキストを挿入できませんでした。  <br/> |
|hrPageObjectDoesNotExist  <br/> |0x8004200e  <br/> |Page オブジェクトは存在しません。  <br/> |
|hrBinaryObjectDoesNotExist  <br/> |0x8004200f  <br/> |バイナリ オブジェクトが存在しません。  <br/> |
|hrLastModifiedDateDidNotMatch  <br/> |0x80042010  <br/> |最終更新日が一致しません。  <br/> |
|hrGroupDoesNotExist  <br/> |0x80042011  <br/> |セクション グループが存在しません。  <br/> |
|hrPageDoesNotExistInGroup  <br/> |0x80042012  <br/> |ページは、セクション グループ内に存在しません。  <br/> |
|hrNoActiveSelection  <br/> |0x80042013  <br/> |アクティブな選択項目はありません。  <br/> |
|hrObjectDoesNotExist  <br/> |0x80042014  <br/> |オブジェクトが存在しません。  <br/> |
|hrNotebookDoesNotExist  <br/> |0x80042015  <br/> |ノートブックが存在しません。  <br/> |
|hrInsertingFile  <br/> |0x80042016  <br/> |ファイルを挿入できませんでした。  <br/> |
|hrInvalidName  <br/> |0x80042017  <br/> |名前が正しくありません。  <br/> |
|hrFolderDoesNotExist  <br/> |0x80042018  <br/> |(セクション グループ) のフォルダーが存在しません。  <br/> |
|hrInvalidQuery  <br/> |0x80042019  <br/> |クエリが正しくありません。  <br/> |
|hrFileAlreadyExists  <br/> |0x8004201a  <br/> |ファイルは既に存在します。  <br/> |
|hrSectionEncryptedAndLocked  <br/> |0x8004201b  <br/> |セクションは暗号化され、ロックされています。  <br/> |
|hrDisabledByPolicy  <br/> |0x8004201c  <br/> |アクションは、ポリシーによって無効になります。  <br/> |
   
||||
|:-----|:-----|:-----|
|hrNotYetSynchronized  <br/> |0x8004201d  <br/> |OneNote のコンテンツはまだ同期されていません。  <br/> |
|hrLegacySection  <br/> |0x8004201E  <br/> |セクションは OneNote 2007 または以前のバージョンが。  <br/> |
|hrMergeFailed  <br/> |0x8004201F  <br/> |マージ操作が失敗しました。  <br/> |
|hrInvalidXMLSchema  <br/> |0x80042020  <br/> |XML スキーマが無効です。  <br/> |
|hrFutureContentLoss  <br/> |0x80042022  <br/> |(将来のバージョンの OneNote) は、コンテンツの損失が発生しました。  <br/> |
|hrTimeOut  <br/> |0x80042023  <br/> |操作がタイムアウトしました。  <br/> |
|hrRecordingInProgress  <br/> |0x80042024  <br/> |オーディオの録音中です。  <br/> |
|hrUnknownLinkedNoteState  <br/> |0x80042025  <br/> |リンクされたノートの状態は認識されません。  <br/> |
|hrNoShortNameForLinkedNote  <br/> |0x80042026  <br/> |リンクされたノートの短い形式の名前が存在しません。  <br/> |
|hrNoFriendlyNameForLinkedNote  <br/> |0x80042027  <br/> |リンクされたノートのフレンドリ名が存在しません。  <br/> |
|hrInvalidLinkedNoteUri  <br/> |0x80042028  <br/> |メモ リンクされた URI は無効です。  <br/> |
|hrInvalidLinkedNoteThumbnail  <br/> |0x80042029  <br/> |サムネイル リンク ノートが正しくありません。  <br/> |
|hrImportLNTThumbnailFailed  <br/> |0x8004202A  <br/> |サムネイルのリンク ノートのインポートに失敗しました。  <br/> |
|hrUnreadDisabledForNotebook  <br/> |0x8004202B  <br/> |ノートブックの未読の強調表示が無効になります。  <br/> |
|hrInvalidSelection  <br/> |0x8004202C  <br/> |選択範囲が正しくありません。  <br/> |
|hrConvertFailed  <br/> |0x8004202D  <br/> |変換に失敗しました。  <br/> |
|hrRecycleBinEditFailed  <br/> |0x8004202E  <br/> |ごみ箱の編集に失敗しました。  <br/> |
   
OneNote 2013の新しいエラー コードを以下に示します。
  
|**HRESULT 型**|**値**|**Description**|
|:-----|:-----|:-----|
|hrIMConversationTypeInvalid  <br/> |0x8004202F  <br/> |**IMConversationType**ページのノードが 0,1,2 または 3 以外の値にする場合は、 **UpdatePageContent**によって返される  <br/> |
|hrAppInModalUI  <br/> |0x80042030  <br/> |モーダル ダイアログ ボックスは、アプリケーションをブロックされています。  <br/> |
   
## <a name="see-also"></a>関連項目

- [OneNote の開発者用リファレンス](onenote-developer-reference.md)

