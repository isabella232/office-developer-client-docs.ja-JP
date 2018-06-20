---
title: アドレス帳を検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6673e1d51a7c030a35a7c5c3cbc955341afba299
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803856"
---
# <a name="searching-the-address-book"></a>アドレス帳を検索

**適用されます**: Outlook 
  
MAPI �ł́A�����@�\�� 2 �̃��x�����������A�h���X���̃v���o�C�_�[���L���ɂ��܂��B
  
- アドレス帳のエントリの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを使用して指定した名前に一致する基本的なレベルです。 このレベルでは、ユーザー、たとえば、北西で始まる名前の配布リストを表示またはブラウンは個々 のメッセージングのユーザーを検索します。
    
- ���x�� **PR_DISPLAY_NAME**�ȊO�̃v���p�e�B�Ɉ�v���܂��B���̃��x���ɂ́A���b�Z�[�W���O����Ƃ������O�̎�ނ����̃A�h���X�ƃ��[�U�[�̌����ƌ�����i�荞�ނȂǁA���[�U�[���ł��܂��B
    
アドレス帳プロバイダーでは、両方のレベルで、基本的なレベルでは、そのコンテナーのそれぞれの検索をサポートしたり、まったくサポートしないように選択することが、ためにしない標準機能として実装することを検索します。 特定のコンテナーが検索をサポートしているかどうかは、その[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)メソッドの呼び出しで検索条件を確立するためにしようとします。 **SetSearchCriteria**では、MAPI_E_NO_SUPPORT が返された場合、コンテナーは、検索をサポートしていません。 
  
検索をサポートするコンテナー、 [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md)を呼び出すことによって確立された条件を取得します。 コンテナーの内容のテーブルが表示される前に、ユーザーを検索条件を求められる点を要求することもできます。 このオプションを選択するには、コンテナーの**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) のプロパティの AB_FIND_ON_OPEN フラグを設定します。 抽出条件を入力すると後、は、制限として保存され、 **SetSearchCriteria**メソッドに渡されることが。 設定 AB_FIND_ON_OPEN は、オンライン サービス、またはそのデータを低速リンクしているすべてのアドレス帳プロバイダーを使用する場合に特に便利です。 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>アドレス帳コンテナーの基本的な検索を実行するには
  
1. ���̓�e�̃e�[�u����J�����߂̃R���e�i�[��[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)���\�b�h��Ăяo���܂��B 
    
2. �j�[�Y�ɍ������������@��I����܂��B[�I����ڂ͎��̂Ƃ���ł��B
    
   - �\��̓���̍s���������[IMAPITable::FindRow](imapitable-findrow.md)�ɂ��܂��B 
    
   - �e�[�u���̍s�̏�����[IMAPITable::SortTable](imapitable-sorttable.md)�ɂ��܂��B 
    
   - �\�`���r���[�𐧌�����[IMAPITable::Restrict](imapitable-restrict.md)�ɂ��܂��B 
    
   - プロパティのあいまいな名前を解決するため、 **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティを使用して制限します。 この制限を課すために**IMAPITable::Restrict**を呼び出します。 
    
   - �����܂��Ȗ��O��������̂ɂ�[IABContainer::ResolveNames](iabcontainer-resolvenames.md)�ɂ��܂��B 
    
3. �K�p���ꂽ��������Ɉ�v���邷�ׂĂ̍s��擾����[IMAPITable::QueryRows](imapitable-queryrows.md)���₢���킹���������B **QueryRows**�ɂ́A1 �ȏ�̈�v����s��Ԃ����Ƃ��ł��܂��B 
    
**FindRow**、 **SortTable**、および**Restrict**メソッドは、クライアントまたはサービス プロバイダーによって作成できる任意のテーブルで利用可能なテーブルのメソッドです。 **PR\_ANR**プロパティの制限および**IABContainer::ResolveNames**メソッドは、アドレス帳プロバイダーに固有のものし、あいまいな名前を解決するために使用します。 あいまいな名前は、それらに関連付けられている**PR_ENTRYID**プロパティを持たない受信者リスト内のエントリです。 
  
**PR\_ANR**制限は、文字の文字列を単語に分割し、プレフィックス一致を使用してアドレス帳の情報を使用してこれらの単語と一致するアルゴリズムを起動します。 一致するのに使用される情報は、アドレス帳プロバイダーに依存します。 アドレス帳コンテナーの**PR_ANR**の制限をサポートするすべてのアドレス帳プロバイダーが必要です。 詳細については、[名前解決の実装](implementing-name-resolution.md)を参照してください。
  
**IABContainer::ResolveNames**は、 **PR_ANR**の制限がコンテナーの内容のテーブルを開くことを必要とせず、複数の名前で処理を実行します。 呼び出すよりもはるかに高速にすることができます複数の名前を解決するのには**ResolveNames**を 1 回の呼び出し、 **PR\_ANR**複数回に制限します。 ただし、アドレス帳プロバイダーは、 **ResolveNames**をサポートする必要はありません。
  

