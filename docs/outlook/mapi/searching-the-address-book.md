---
title: アドレス帳の検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 59a82ff1ab8880fc89b3195f4631a74923b41722
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599012"
---
# <a name="searching-the-address-book"></a>アドレス帳の検索

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI �ł́A�����@�\�� 2 �̃��x�����������A�h���X���̃v���o�C�_�[���L���ɂ��܂��B
  
- アドレス帳エントリの PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティと **指定** した名前に一致する基本レベル。 このレベルでは、たとえば、名前がノースウエストで始まる配布リストを表示したり、名が Brown の個々のメッセージング ユーザーを見つけるなどできます。
    
- ���x�� **PR_DISPLAY_NAME**�ȊO�̃v���p�e�B�Ɉ�v���܂��B���̃��x���ɂ́A���b�Z�[�W���O����Ƃ������O�̎�ނ����̃A�h���X�ƃ��[�U�[�̌����ƌ�����i�荞�ނȂǁA���[�U�[���ł��܂��B
    
Because address book providers can support searching for each of their containers at the basic level, at both levels, or choose not to support it at all, do not expect searching to be implemented as a standard feature. To determine if a particular container supports searches, attempt to establish search criteria in a call to its [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. If **SetSearchCriteria** returns MAPI_E_NO_SUPPORT, the container does not support searches. 
  
In a container that supports searches, retrieve established criteria by calling [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md). You can also request that the user be prompted for search criteria before a container's contents table is displayed. このオプションを選択するには、コンテナー AB_FIND_ON_OPEN **(** [PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティPR_CONTAINER_FLAGSフラグを設定します。 After the user enters the criteria, it is stored as a restriction and passed to the **SetSearchCriteria** method. Setting AB_FIND_ON_OPEN is particularly useful if you are using an online service or any address book provider that has a slow link to its data. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>�A�h���X���R���e�i�[�̊�{�I�Ȍ�������s����ɂ�
  
1. ���̓�e�̃e�[�u����J�����߂̃R���e�i�[��[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)���\�b�h��Ăяo���܂��B 
    
2. �j�[�Y�ɍ������������@��I����܂��B[�I����ڂ͎��̂Ƃ���ł��B
    
   - �\��̓���̍s���������[IMAPITable::FindRow](imapitable-findrow.md)�ɂ��܂��B 
    
   - �e�[�u���̍s�̏�����[IMAPITable::SortTable](imapitable-sorttable.md)�ɂ��܂��B 
    
   - �\�`���r���[�𐧌�����[IMAPITable::Restrict](imapitable-restrict.md)�ɂ��܂��B 
    
   - あいまいな名前を **解決PR_ANR** プロパティ ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティを使用するプロパティ制限。 **IMAPITable::Restrict を呼び出して**、この制限を適用します。 
    
   - �����܂��Ȗ��O��������̂ɂ�[IABContainer::ResolveNames](iabcontainer-resolvenames.md)�ɂ��܂��B 
    
3. �K�p���ꂽ��������Ɉ�v���邷�ׂĂ̍s��擾����[IMAPITable::QueryRows](imapitable-queryrows.md)���₢���킹���������B **QueryRows**�ɂ́A1 �ȏ�̈�v����s��Ԃ����Ƃ��ł��܂��B 
    
The **FindRow**, **SortTable**, and **Restrict** methods are table methods that are available for any table that can be created, either by a client or a service provider. **PR \_ ANR プロパティ** の制限と **IABContainer::ResolveNames** メソッドはアドレス帳プロバイダーに固有のメソッドであり、あいまいな名前の解決に使用されます。 Ambiguous names are entries in a recipient list that do not have a **PR_ENTRYID** property associated with them. 
  
**PR \_ ANR 制限は**、文字列を単語に分け、プレフィックス一致を使用してアドレス帳内の情報と一致するアルゴリズムを呼び出します。 The information used for the matching depends on the address book provider. All address book providers are required to support the **PR_ANR** restriction for their address book containers. For more information, see [Implementing Name Resolution](implementing-name-resolution.md).
  
**IABContainer::ResolveNames** は、コンテナー **PR_ANR** テーブルを開く必要なしに、複数の名前に対して制限処理を実行します。 **ResolveNames を 1** 回呼び出して複数の名前を解決すると **、PR \_ ANR** 制限を複数回呼び出すよりもはるかに高速になります。 ただし、アドレス帳プロバイダーは **ResolveNames をサポートする必要はありません**。
  

