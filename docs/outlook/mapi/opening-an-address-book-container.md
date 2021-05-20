---
title: アドレス帳のコンテナーを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: '最終更新日: 2011 年 11 月 08 日'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436742"
---
# <a name="opening-an-address-book-container"></a>アドレス帳のコンテナーを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 統合アドレス帳を開いた後、1 つ以上のアドレス帳コンテナーを開いて、その中の受信者にアクセスします。
  
アドレス帳のトップ レベル コンテナーを開く場合は、NULL エントリ識別子を使用して [IAddrBook::OpenEntry](iaddrbook-openentry.md) を呼び出します。 
  
アドレス帳コンテナーは、読み取り専用または読み取り/書き込みアクセスで実装できます。 読み取り専用コンテナーは、参照にのみ使用されます。 読み取り/書き込みコンテナーは変更でき、クライアントは新しいエントリを作成し、既存のエントリを削除および変更できます。 すべての個人用アドレス帳 (PAB) コンテナーは、読み取り/書き込みコンテナーとして実装されます。 
  
下位レベルのコンテナーを開く場合は **、OpenEntry** を呼び出し、開くコンテナーのエントリ識別子を指定します。 
  
## <a name="open-the-container-designated-as-the-pab"></a>PAB として指定されているコンテナーを開く
  
1. [IAddrBook::GetPAB](iaddrbook-getpab.md)を呼び出して、PAB のエントリ識別子を取得します。 
    
2. このエントリ識別子を [IAddrBook::OpenEntry に渡します](iaddrbook-openentry.md)。
    
## <a name="open-a-container-that-is-not-the-pab"></a>PAB ではないコンテナーを開く
  
1. アドレス帳のルート コンテナーを開く NULL エントリ識別子を使用して [IAddrBook::OpenEntry](iaddrbook-openentry.md) を呼び出します。 
    
2. ルート コンテナーの [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) メソッドを呼び出して、その階層テーブル (アドレス帳内のすべてのトップ レベル コンテナーのリスト) を取得します。 
    
3. 開くコンテナーが特定の種類の場合:
    
   - プロパティ タグの **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))、プロパティ値のコンテナーの型、およびリレーションの RELOP_EQ を持つ **SPropertyRestriction** 構造体を作成します。 **PR_DISPLAY_TYPE** は、次の中で多数の値に設定できます。 
    
   - DT_GLOBAL、階層テーブルをグローバル アドレス一覧に属するコンテナーに制限します。
    
   - DT_LOCALアドレス帳に属するコンテナーにテーブルを制限する必要があります。
    
   - DT_MODIFIABLE変更可能なコンテナーにテーブルを制限する必要があります。
    
   - [SPropTagArray](sproptagarray.md)構造体を作成し **、PR_ENTRYID、PR_DISPLAY_TYPE** その **他** の列を含む構造を作成します。 
    
   - [HrQueryAllRows を呼び](hrqueryallrows.md)出し、プロパティ制限とプロパティ タグ配列を渡します。 **HrQueryAllRows は** 、指定した型に属するコンテナーごとに 0 行以上の行を返します。 任意の数の行の戻り値を処理する準備をしてください。 
    
   - **IAddrBook::OpenEntry** を呼び出し **、** 関心のあるコンテナーを表す行の PR_ENTRYID 列のエントリ識別子を使用します。 
    
4. 開くコンテナーが特定のアドレス帳プロバイダーに属している場合:
    
   - プロパティ タグの **PR_AB_PROVIDERS** ([PidTagAbProviders)、](pidtagabproviders-canonical-property.md)プロパティ値のプロバイダー固有の値、およびリレーションの RELOP_EQ を持つ [SPropertyRestriction](spropertyrestriction.md)構造体を作成します。 通常、プロバイダー固有の値は、グローバルに一意の識別子または GUID です。 この値は、アドレス帳プロバイダーのヘッダー ファイルの 1 つで公開されています。 
    
   - [SPropTagArray](sproptagarray.md)構造体を作成 **し**、PR_ENTRYID ([PidTagEntryId)](pidtagentryid-canonical-property.md)、PR_AB_PROVIDERS、その **他** の関心のある列を含む構造を作成します。 
    
   - [HrQueryAllRows を呼び](hrqueryallrows.md)出し、プロパティ制限とプロパティ タグ配列を渡します。 指定したアドレス帳プロバイダーがプロファイルに含めされていない場合 **、HrQueryAllRows** は 0 行を返します。 プロバイダーの整理方法に応じて、プロバイダーのトップ レベル コンテナーに対して 1 つ以上の行を返す場合があります。 
    
   - [IAddrBook::OpenEntry](iaddrbook-openentry.md)を呼び出し **、** 関心のあるコンテナーを表す行の PR_ENTRYID 列のエントリ識別子を使用します。 関心のあるコンテナーがトップ レベル のコンテナーではない場合は、トップ レベルのコンテナーを見つけて、階層を走査します。 
    

