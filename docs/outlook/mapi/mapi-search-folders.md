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
ms.openlocfilehash: b5a95ca77496c3c4c2d28641ab649c2b4328a27c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578557"
---
# <a name="mapi-search-folders"></a>MAPI �����t�H���_�[

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
�������ʂ̃t�H���[�[�ł́A���ۂ̃��b�Z�[�W�ł͂Ȃ��A��ʓI�ȃt�H���](imapifolder-createfolder.md)�[��̃��b�Z�[�W�ւ̃����N��ێ����܂��B�N���C�A���g�ł́A  _ulFolderType_�p�����[�^�[�Ƃ��� FOLDER_SEARCH [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)���\�b�h��g�p���Č������ʂ̃t�H���[�[��쐬���܂��B�N���C�A���g�̃Z�b�g�A�b�v�ƌ��������K�p���āA�������ʂ̃t�H���](imapicontainer-setsearchcriteria.md)�[����͂���: ���[�������̓���������郁�b�Z�[�W��t�B���^�[�������܂��B���������[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)���\�b�h��g�p���ăZ�b�g�A�b�v���܂��B�N���C�A���g�ł́A���������K�p���āA [SetSearchCriteria](srestriction.md)�ɓn����\�� 1 �܂��͕�����**SRestriction**�\����쐬���܂��B **SetSearchCriteria**������h���C��������t�H���_�[�̈ꗗ����уZ�b�g��w�肷��t���O�̌�������s������@�𐧌䂵�܂��B 
  
 **SetSearchCriteria**は、指定した制限に一致するメッセージを識別します。 選択したメッセージ (条件を満たすもの) は、検索結果フォルダー内のリンクとして表示されます。 クライアントは、検索結果フォルダーの内容にアクセスするのには[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出して、テーブルで選択したメッセージが表示されます。 検索結果フォルダーの内容のテーブルには、汎用フォルダーの内容のテーブルと同じ列が含まれています。 ただし、 **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) のプロパティは、検索結果フォルダーの場合は、リンクされているメッセージが格納されているフォルダーのエントリ id を指定します。 検索結果フォルダーは、親フォルダーとは見なされません。
  
�t�H���_�[�̌������ʂł́A���̐�������������܂��B
  
- **SetSearchCriteria**を呼び出すことによっては、検索結果フォルダーの内容を変更できることを唯一の方法です。 **SetSearchCriteria**の実装の詳細については、サポート技術情報 279095 を参照してください[260322: どのようにする検索フォルダーの SetSearchCriteria メソッドを使用して](http://go.microsoft.com/fwlink/?LinkId=123603)。
    
- ���b�Z�[�W��ړ��܂��͌������ʂ̃t�H���_�[�ɃR�s�[���邱�Ƃ͂ł��܂���B
    
- 検索結果フォルダーのサブフォルダーを含めることはできません。 
    
- �N���C�A���g�ł́A�����̌�����������ʂ̃t�H���_�[��s�����Ƃ͂ł��܂���B
    
ただし、検索結果フォルダーのプロパティを変更して、メッセージを削除することです。 検索結果のフォルダーからメッセージが削除されると、実際には実際のフォルダーから削除されます。 ただし、検索結果フォルダー自体を削除するのには影響しません; 中のメッセージ一般的なフォルダーに残ります。
  
## <a name="see-also"></a>�֘A����



[MAPI �t�H���_�[](mapi-folders.md)

