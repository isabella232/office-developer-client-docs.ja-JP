---
title: 複数の Exchange アカウントの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: '最終更新日: 2012 年 6 月 25 日'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329654"
---
# <a name="using-multiple-exchange-accounts"></a>複数の Exchange アカウントの使用

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 および Microsoft Outlook 2013 では、複数の Exchange 電子メール アカウントの統合をサポートしています。 Outlook 2010 または Outlook 2013 では、ユーザーは 2 つの Exchange アカウントを同一のプロファイルに追加できます。その場合も、Exchange の豊富な機能 (公開されたグローバル アドレス一覧 (GAL)、Exchange の不在時構成、フォルダー共有など) は、そのまま使用できます。
  
Microsoft Office Outlook 2007 以前の MAPI プロファイルの各セクションに詳しいユーザーは、Exchange の設定 (ユーザー名やサービス名など) が固定の Exchange グローバル プロファイル セクション **pbGlobalProfileSectionGuid** に保存されていることを知っています。 Outlook 2010 および Outlook 2013 では、設定を保存するための専用のプロファイル セクションが、それぞれの Exchange アカウントに必要になるため、**pbGlobalProfileSectionGuid** は使用されなくなりました。 
  
Outlook 2010 および Outlook 2013 の Exchange 設定は、以前と同様にプロファイルに保存されますが、その設定を格納しているプロファイル セクションにはプロファイルごとに動的に一意識別子が割り当てられます。プロファイルに収められた Exchange 設定の場所は、[PidTagExchangeProfileSectionId 標準プロパティ](pidtagexchangeprofilesectionid-canonical-property.md)に保存されていて、Exchange アカウントのメッセージ サービス プロファイル セクションで確認できます。また、このプロパティは、このアカウントのメッセージ サービスの各プロバイダーに対応するプロファイル セクションでも確認できます。一意識別子は、サーバーには保存されず、プロファイル間で異なるものになります。
  
Outlook 2010 および Outlook 2013 では、Exchange アカウントを特定する一意識別として **PidTagExchangeProfileSectionId** が使用されます。この目的に使用される場合、この一意識別子は **emsmdbUID** と呼ばれます。MAPI および Outlook の一部の操作では、その操作に使用する Exchange アカウントを指定するために、**emsmdbUID** が必要になることがあります。 
  
複数の Exchange アカウントをサポートするために、いくつかの新しい関数の呼び出しをコード内で使用する必要があります。**entryID** と、[IMailUser : IMAPIProp](imailuserimapiprop.md) および [IDistList : IMAPIContainer](idistlistimapicontainer.md) の [IAddrBook::OpenEntry](iaddrbook-openentry.md) または [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) を使用する呼び出しがあれば、その呼び出しを次のいずれかに置き換えます。 
  
- [HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
    
- [HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
    
- [HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
    
- [HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
    
- [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
    
- [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
    
- [HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
    
- [HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
    
- [HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a>レガシ サポート

この新しい **emsmdbUID** セクションが現れる前に作成された MAPI クライアントは、引き続きサポートされます。このようなクライアントは、これまでどおりに以前のグローバル セクション **pbGlobalProfileSectionGuid** を取得します。このプロファイル セクションに対するクエリは、従来のクエリを処理する指定された 1 つの Exchange アカウントにリダイレクトされます。この従来の呼び出しを処理するアカウントは、メッセージ サービス テーブルを調べて、PR_EMSMDB_LEGACY の列を追加することで判断できます。これが true に設定されているメッセージ サービスは 1 つのみであり、そのサービスの **PidTagExchangeProfileSectionId** は従来の **emsmdbUID** と呼ばれます。
  
> [!NOTE]
> 構成可能な MAPI 設定 (既定のストアや既定のアカウントなど) は、どのアカウントが従来の呼び出しを処理するかについて影響しません。従来の呼び出しを処理するアカウントは構成できません。 
  
従来のアカウントの **emsmdbUID** は、Outlook グローバル プロファイル セクションにコピーされます。このプロパティが存在しない場合は、メッセージ サービス テーブルをクエリすることで、どのアカウントがレガシ ハンドラであるかを判断して、その値を Outlook グローバル プロファイル セクションで設定します。 
  
明確に説明すると、Outlook グローバル プロファイル セクションは Exchange グローバル プロファイル セクションとは別のものであり、Outlook 2010 および Outlook 2013 の Exchange グローバル プロファイル セクションは、複数の Exchange アカウントを持てるようになったため、実際にはグローバルではなくなっています。Outlook グローバル プロファイル セクションには、Outlook に関するプロパティ (フォルダー MRU の状態やグローバル接続の状態など) が含まれています。
  
## <a name="address-book-account-contexts"></a>アドレス帳アカウントのコンテキスト

複数の Exchange アカウントでアドレスを正しく解決するには、アカウントのコンテキストを取得する新しい関数を使用して、アドレス帳の呼び出しで正しい Exchange アカウントを検索するようにします。
  
以前のアドレス帳 API の一部は、複数の Exchange に完全には対応していなかったため使用されなくなりました。通常、このアカウントのコンテキストは **emsmdbUID** になります。
  
この **emsmdbUID** に加えて、複数の Exchange アカウントには **emsabpUID** もあります。
  
1. **emsmdbUID** の値では、アカウントのコンテキストを識別します。 
    
2. **emsabpUID** の値では、Exchange アドレス帳プロバイダーを識別します。 
    
通常、**emsabpUID** の値は受信者を解決するときに使用されます。受信者の解決に [IAddrBook::ResolveName](iaddrbook-resolvename.md) を使用すると、Exchange の受信者行には **PR_AB_PROVIDERS** (0x3D010102) プロパティが格納されます。**emsabpUID** の値は、このプロパティに格納されています。**emsabpUID** の値によって、特定の受信者の Exchange アドレス帳プロバイダーを識別します。 
  
特定の **emsmdbUID** に対応する **emsabpUID** の値を調べるには、その **emsmdbUID** のプロファイル セクションを開いて、**PR_EMSABP_USER_UID** (0x0x3D1A0102) プロパティを取得します。 
  
[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) を呼び出す場合は、その呼び出しで渡すリスト内の Exchange の受信者に、**PR_AB_PROVIDERS** プロパティが含まれていて、その受信者が属するアドレス帳プロバイダーと一致する **emsabpUID** が保持されていることを確認してください。[IAddrBook::ResolveName](iaddrbook-resolvename.md) から取得した行に対して [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) を呼び出す場合は追加のアクションは不要ですが、一部のコードでは **PR_ENTRYID** プロパティのみが含まれる行に対して [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) を呼び出すことになります。このような状況の行には、**PR_AB_PROVIDERS** プロパティが正しい **emsabpUID** に設定されている **PR_ENTRYID** と **PR_AB_PROVIDERS** の両方が格納されている必要があります。
  
複数の Exchange アカウントを解決するためのプロセスについて、簡単な説明を次に示します。
  
- サービスの一意識別子がある場合は、コードで、その識別子と一致する **PR_SERVICE_UID** プロパティのメッセージ ストアのテーブルを調べます。正しい **PR_MDB_PROVIDER** は、そこで判断できます。この行には、適切なストアが格納されています。
    
- **emsmdbUID** がある場合は、コードで、その **emsmdbUID** と一致する **PidTagExchangeProfileSectionId** を公開している行についてメッセージ サービス テーブルを調べます。
    
## <a name="see-also"></a>関連項目



[HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
  
[HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
  
[HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
  
[HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
  
[HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
  
[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
  
[HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
  
[HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
  
[HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
  
[HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
  
[PidTagExchangeProfileSectionId 標準プロパティ](pidtagexchangeprofilesectionid-canonical-property.md)


[グローバル プロファイル セクションを開く方法](https://support.microsoft.com/kb/188482)

