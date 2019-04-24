---
title: MAPI �����t�H���_�[
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 36c14d91-77f7-43a3-8d87-d50bcc21fad7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c1d7f67458852319587d98831d031b2c3a131871
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357674"
---
# <a name="mapi-search-folders"></a>MAPI �����t�H���_�[

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
検索結果フォルダーには、実際のメッセージではなく汎用フォルダー内のメッセージへのリンクが格納されます。 クライアントは、 _ulfoldertype_パラメーターとして FOLDER_SEARCH を指定して[imapifolder:: CreateFolder](imapifolder-createfolder.md)メソッドを呼び出すことによって、検索結果フォルダーを作成します。 クライアントは、検索条件を設定して適用することにより、検索結果フォルダーをいっぱいにします。特定の特性を持つメッセージを除外するルール。 [IMAPIContainer:: setsearchcriteria](imapicontainer-setsearchcriteria.md)メソッドを使用して、検索条件を設定します。 クライアントは、適用する検索条件を表す1つまたは複数の[srestriction](srestriction.md)構造を構築し、それらを**setsearchcriteria**に渡します。 **setsearchcriteria**では、検索ドメインおよび検索の実行方法を制御するフラグのセットを示すフォルダーの一覧も指定します。 
  
 **SetSearchCriteria** identifies the messages that match the specified restriction. The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder. When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table. Contents tables for search-results folders contain the same columns as contents tables for generic folders. ただし、検索結果フォルダーの場合、 **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) プロパティは、リンクされたメッセージが存在するフォルダーのエントリ識別子を指定します。 Search-results folders are not considered parent folders.
  
�t�H���_�[�̌������ʂł́A���̐�������������܂��B
  
- The only way that the contents of a search-results folder can be modified is through a call to **SetSearchCriteria**. For more information about the implementation of **SetSearchCriteria**, see Knowledge Base article [260322: How To Search Folders with the SetSearchCriteria Method](https://go.microsoft.com/fwlink/?LinkId=123603).
    
- ���b�Z�[�W��ړ��܂��͌������ʂ̃t�H���_�[�ɃR�s�[���邱�Ƃ͂ł��܂���B
    
- Search-results folders cannot contain subfolders. 
    
- �N���C�A���g�ł́A�����̌�����������ʂ̃t�H���_�[��s�����Ƃ͂ł��܂���B
    
It is possible, however, to modify the properties of a search-results folder and use it to delete a message. When a message is deleted from a search-results folder, it is actually deleted from the real folder. However, deleting the search-results folder itself has no impact on the messages inside; they remain in their generic folders.
  
## <a name="see-also"></a>関連項目



[MAPI �t�H���_�[](mapi-folders.md)

