---
title: アドレス帳コンテナーを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: 28f60154524065bd2c818e2e4b7db37ca33276b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801690"
---
# <a name="opening-an-address-book-container"></a>アドレス帳コンテナーを開く

**適用されます**: Outlook 
  
MAPI を開くには、アドレス帳が統合されて後、は、1 つまたは複数のアドレス帳コンテナー内の受信者にアクセスを開きます。
  
アドレス帳の最上位のコンテナーを開くには、NULL のエントリの識別子を使用して[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。 
  
読み取り専用のアドレス帳コンテナーを実装することができますまたは読み取り/書き込みアクセス。 読み取り専用コンテナーは、参照用にのみ使用されます。 クライアントが新しいエントリを作成、削除および既存のエントリを変更できるように、読み取り/書き込みのコンテナーを変更できます。 個人用アドレス帳 (PAB) のすべてのコンテナーは、コンテナーの読み取り/書き込みとして実装されます。 
  
より低いレベルのコンテナーを開くには、 **OpenEntry**を呼び出すし、開かれるコンテナーのエントリの識別子を指定します。 
  
## <a name="open-the-container-designated-as-the-pab"></a>個人アドレス帳として指定されているコンテナーを開く
  
1. 個人用アドレス帳のエントリの識別子を取得する[られたユーザーのプライマリ](iaddrbook-getpab.md)を呼び出します。 
    
2. [アドレス帳コンテナー](iaddrbook-openentry.md)には、このエントリの識別子を渡します。
    
## <a name="open-a-container-that-is-not-the-pab"></a>個人アドレス帳ではないコンテナーを開く
  
1. 開くには、アドレス帳のルート コンテナーの NULL エントリ識別子を使用して[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。 
    
2. 階層テーブルを取得するのには、ルート コンテナーの[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出して、アドレス帳内の最上位のコンテナーのすべてのリスト。 
    
3. 場合は、コンテナーを開くには、特定の種類のです。
    
   - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) を持つプロパティ タグは、コンテナーの値の型、プロパティ、関係の RELOP_EQ の**SPropertyRestriction**構造体を作成します。 **PR_DISPLAY_TYPE**は、それらの間、多くの値を設定できます。 
    
   - グローバル アドレス一覧に属しているコンテナーの階層テーブルを制限する DT_GLOBAL です。
    
   - コンテナーがローカルのアドレス帳に所属するテーブルを制限する DT_LOCAL です。
    
   - 変更可能なコンテナーにテーブルを制限する DT_MODIFIABLE です。
    
   - **PR_ENTRYID**、 **PR_DISPLAY_TYPE**、および興味の他のすべての列を含む[SPropTagArray](sproptagarray.md)構造体を作成します。 
    
   - [HrQueryAllRows](hrqueryallrows.md)で、プロパティの制限とプロパティ タグ配列を渡してを呼び出します。 **HrQueryAllRows**は、0 個または複数の行、指定した型に属するすべてのコンテナーの 1 つの行が返されます。 行の任意の数の戻り値を処理するために準備します。 
    
   - 目的のコンテナーを表す行の**PR_ENTRYID**列のエントリの識別子を使用して**アドレス帳コンテナー**を呼び出します。 
    
4. 場合は、コンテナーを開くには、特定のアドレス帳プロバイダーに属します。
    
   - プロパティ タグ、プロパティの値として、プロバイダー固有の値との関係の RELOP_EQ の**PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) と、 [SPropertyRestriction](spropertyrestriction.md)構造体を作成します。 通常プロバイダー固有の値は、グローバルに一意の識別子または GUID です。 アドレス帳プロバイダーのヘッダー ファイルのいずれかで公開されているこの値が表示されます。 
    
   - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_AB_PROVIDERS**、および興味の他のすべての列を含む[SPropTagArray](sproptagarray.md)構造体を作成します。 
    
   - [HrQueryAllRows](hrqueryallrows.md)で、プロパティの制限とプロパティ タグ配列を渡してを呼び出します。 プロファイルで指定したアドレス帳プロバイダーがない場合は、 **HrQueryAllRows**を 0 個の行に戻ります。 プロバイダーの構成方法に応じて、プロバイダーの最上位のコンテナーの 1 つまたは複数の行を返すことです。 
    
   - 目的のコンテナーを表す行の**PR_ENTRYID**列のエントリの識別子を使用して[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。 興味があることをコンテナーが最上位のコンテナーでない場合は、最上位のコンテナーを検索し、階層を移動します。 
    

