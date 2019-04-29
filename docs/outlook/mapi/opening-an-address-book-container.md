---
title: アドレス帳のコンテナーを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: '最終更新日: 2011 年11月8日'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436742"
---
# <a name="opening-an-address-book-container"></a>アドレス帳のコンテナーを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 統合アドレス帳を開いたら、1つ以上のアドレス帳コンテナーを開いて、その内部の受信者にアクセスします。
  
アドレス帳のトップレベルのコンテナーを開くには、NULL エントリ識別子を持つ[IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出します。 
  
アドレス帳コンテナーは、読み取り専用または読み取り/書き込みアクセスで実装できます。 読み取り専用コンテナーは、参照にのみ使用されます。 読み取り/書き込みコンテナーを変更して、クライアントが新しいエントリを作成したり、既存のエントリを削除したり、変更したりできるようにすることができます。 すべての個人用アドレス帳 (PAB) コンテナーは、読み取り/書き込みコンテナーとして実装されます。 
  
任意の下位レベルのコンテナーを開くには、 **openentry**を呼び出し、開くコンテナーのエントリ識別子を指定します。 
  
## <a name="open-the-container-designated-as-the-pab"></a>PAB として指定されたコンテナーを開きます。
  
1. [IAddrBook:: getpab](iaddrbook-getpab.md)を呼び出して、pab のエントリ識別子を取得します。 
    
2. このエントリ識別子を[IAddrBook:: openentry](iaddrbook-openentry.md)に渡します。
    
## <a name="open-a-container-that-is-not-the-pab"></a>PAB ではないコンテナーを開く
  
1. [IAddrBook::](iaddrbook-openentry.md) NULL エントリ識別子を持つ openentry を呼び出して、アドレス帳のルートコンテナーを開きます。 
    
2. ルートコンテナーの[IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出して、その階層テーブルを取得します。これには、アドレス帳のすべてのトップレベルコンテナーのリストが含まれます。 
    
3. 開くコンテナーが特定の種類の場合:
    
   - プロパティタグ、プロパティ値のコンテナーの種類、およびリレーションシップの RELOP_EQ に対して、 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) を使用して**spropertyrestriction**構造を作成します。 **PR_DISPLAY_TYPE**には、複数の値を設定できます。 
    
   - DT_GLOBAL は、階層テーブルをグローバルアドレス一覧に含まれるコンテナーに制限します。
    
   - DT_LOCAL は、ローカルアドレス帳に属するコンテナーにテーブルを制限します。
    
   - DT_MODIFIABLE を使用して、変更可能なコンテナーにテーブルを制限します。
    
   - **PR_ENTRYID**、 **PR_DISPLAY_TYPE**、およびその他の目的の列を含む[SPropTagArray](sproptagarray.md)構造を作成します。 
    
   - [hrqueryallrows](hrqueryallrows.md)を呼び出し、プロパティの制限とプロパティタグの配列を渡します。 **hrqueryallrows**は、0個以上の行を返します。これは、指定された種類に属するすべてのコンテナーにつき1行です。 任意の数の行の戻り値を処理できるように準備します。 
    
   - 目的のコンテナーを表す行の**PR_ENTRYID**列から、エントリ識別子を持つ**IAddrBook:: openentry**を呼び出します。 
    
4. 開くコンテナーが特定のアドレス帳プロバイダーに属している場合:
    
   - プロパティタグに対して**PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) を使用して[spropertyrestriction](spropertyrestriction.md)構造を作成し、プロパティ値にプロバイダー固有の値を指定し、リレーションシップに RELOP_EQ を指定します。 通常、プロバイダー固有の値は、グローバルに一意の識別子または GUID です。 この値は、アドレス帳プロバイダーのヘッダーファイルのいずれかに公開されています。 
    
   - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_AB_PROVIDERS**、およびその他の目的の列を含む[SPropTagArray](sproptagarray.md)構造を作成します。 
    
   - [hrqueryallrows](hrqueryallrows.md)を呼び出し、プロパティの制限とプロパティタグの配列を渡します。 指定したアドレス帳プロバイダーがプロファイルにない場合、 **hrqueryallrows**は0行を返します。 プロバイダーがどのように編成されているかに応じて、プロバイダーの最上位のコンテナーに対して1つ以上の行を返すことができます。 
    
   - 目的のコンテナーを表す行の**PR_ENTRYID**列から、エントリ識別子を持つ[IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出します。 目的のコンテナーが最上位のコンテナーではない場合は、最上位のコンテナーを見つけて、階層をスキャンします。 
    

