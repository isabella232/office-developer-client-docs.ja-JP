---
title: アドレス帳の検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d40419291f4b09c5880a769ce231015511e8f269
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339740"
---
# <a name="searching-the-address-book"></a>アドレス帳の検索

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI �ł́A�����@�\�� 2 �̃��x�����������A�h���X���̃v���o�C�_�[���L���ɂ��܂��B
  
- アドレス帳エントリの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを使用して、指定された名前と一致する基本的なレベル。 このレベルでは、たとえば、北西で始まる名前の配布リストを表示したり、姓が茶色である個々のメッセージングユーザーを検索したりできます。
    
- ���x�� **PR_DISPLAY_NAME**�ȊO�̃v���p�e�B�Ɉ�v���܂��B���̃��x���ɂ́A���b�Z�[�W���O����Ƃ������O�̎�ނ����̃A�h���X�ƃ��[�U�[�̌����ƌ�����i�荞�ނȂǁA���[�U�[���ł��܂��B
    
Because address book providers can support searching for each of their containers at the basic level, at both levels, or choose not to support it at all, do not expect searching to be implemented as a standard feature. To determine if a particular container supports searches, attempt to establish search criteria in a call to its [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. If **SetSearchCriteria** returns MAPI_E_NO_SUPPORT, the container does not support searches. 
  
In a container that supports searches, retrieve established criteria by calling [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md). You can also request that the user be prompted for search criteria before a container's contents table is displayed. このオプションを選択するには、コンテナーの**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティの AB_FIND_ON_OPEN フラグを設定します。 After the user enters the criteria, it is stored as a restriction and passed to the **SetSearchCriteria** method. Setting AB_FIND_ON_OPEN is particularly useful if you are using an online service or any address book provider that has a slow link to its data. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>�A�h���X���R���e�i�[�̊�{�I�Ȍ�������s����ɂ�
  
1. ���̓�e�̃e�[�u����J�����߂̃R���e�i�[��[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)���\�b�h��Ăяo���܂��B 
    
2. �j�[�Y�ɍ������������@��I����܂��B[�I����ڂ͎��̂Ƃ���ł��B
    
   - �\��̓���̍s���������[IMAPITable::FindRow](imapitable-findrow.md)�ɂ��܂��B 
    
   - �e�[�u���̍s�̏�����[IMAPITable::SortTable](imapitable-sorttable.md)�ɂ��܂��B 
    
   - �\�`���r���[�𐧌�����[IMAPITable::Restrict](imapitable-restrict.md)�ɂ��܂��B 
    
   - あいまいな名前の解決に**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティを使用するプロパティ制限。 この制限を課すには、 **IMAPITable:: Restrict**を呼び出します。 
    
   - �����܂��Ȗ��O��������̂ɂ�[IABContainer::ResolveNames](iabcontainer-resolvenames.md)�ɂ��܂��B 
    
3. �K�p���ꂽ��������Ɉ�v���邷�ׂĂ̍s��擾����[IMAPITable::QueryRows](imapitable-queryrows.md)���₢���킹���������B **QueryRows**�ɂ́A1 �ȏ�̈�v����s��Ԃ����Ƃ��ł��܂��B 
    
The **FindRow**, **SortTable**, and **Restrict** methods are table methods that are available for any table that can be created, either by a client or a service provider. **\_PR ANR**プロパティ制限および**IABContainer:: ResolveNames**メソッドは、アドレス帳プロバイダーに固有であり、あいまいな名前の解決に使用されます。 Ambiguous names are entries in a recipient list that do not have a **PR_ENTRYID** property associated with them. 
  
**PR\_ANR**制限は、文字列を単語に分割し、それらの単語をプレフィックス一致を使用してアドレス帳の情報と一致させるアルゴリズムを呼び出します。 The information used for the matching depends on the address book provider. All address book providers are required to support the **PR_ANR** restriction for their address book containers. For more information, see [Implementing Name Resolution](implementing-name-resolution.md).
  
**IABContainer:: ResolveNames**は、コンテナーの contents テーブルを開いていなくても、複数の名前に対して**PR_ANR**制限処理を実行します。 複数の名前を解決するために一度に**ResolveNames**を呼び出しても、 **PR\_ANR**制限を複数回呼び出すよりはるかに高速になります。 ただし、アドレス帳プロバイダーは**ResolveNames**をサポートする必要はありません。
  

