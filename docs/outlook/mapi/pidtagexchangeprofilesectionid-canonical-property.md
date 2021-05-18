---
title: PidTagExchangeProfileSectionId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316430"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>PidTagExchangeProfileSectionId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
複数のアカウントを使用する場合にアカウントを決定するために使用される動的に生成された GUID Microsoft Exchange Serverします。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|識別子:  <br/> |0x3d150102  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |複数の Exchange アカウント  <br/> |
   
## <a name="remarks"></a>注釈

Microsoft Outlook 2010とMicrosoft Outlook 2013 1 つのアカウントではなくExchange複数のアカウントをExchangeできます。 複数のアカウントにExchange、MAPI プロファイル のレイアウトが変更されました。 2007 Microsoft Office Outlook以前では、プロファイルには、サーバー名、ユーザー名、オフライン フォルダー ファイル (.ost) などの Exchange 設定専用の固定プロファイル セクションが含まれるがありました。 場所。 これらの設定は、一意の識別子 **pbGlobalProfileSectionGuid** プロパティを使用して識別されました。 この設定に使用Exchangeセクションは、[グローバル プロファイル] セクションExchange呼び出されます。 
  
固定プロファイル セクションの場所では、複数のアカウントに対応Exchangeなくなりました。 代わりに、プロファイルExchangeアカウントごとに、そのアカウントの設定専用のセクションが存在します。 ユーザー設定に使用される新Exchangeは、一意の識別子 **emsmdbUID によって識別されます**。
  
Exchange アカウントの [メッセージ サービス プロファイル] セクションで、アカウントの作成時に動的に生成される GUID を含むプロパティを検索できます。 この GUID は **、PidTagExchangeProfileSectionId プロパティに格納** されます。 メッセージ ストアとアドレス帳コンテナーは、どのアカウントに属Exchangeプロパティを公開します。 メッセージ サービス テーブルでアクセス可能で、各サービスExchangeこのプロパティを公開します。 
  
次のインターフェイスのクエリを実行した後 **、PidTagExchangeProfileSectionId** の [IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出して、このプロパティを取得できます。 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
オブジェクトがオブジェクトに関連付Exchange場合、呼び出しは次 **MAPI_E_NOT_FOUND。**
  
アドレス帳を表示するときに **、PidTagExchangeProfileSectionId** のコンテナーを制限できます。 コンテナーを開いた後、そのコンテナーから **emsmdbUID を** 照会できます。 また、受信者が Exchange アドレス帳から選択された場合、受信者はプロパティの一覧に **PidTagExchangeProfileSectionId** を持っています。 
  
> [!NOTE]
> コード サンプルと関数ヘッダー全体で、この GUID は **emsmdbUID と呼ばれる。** 
  
既存のアカウントの 1 Exchangeは、従来のアカウントとしてExchangeされます。 通常、プロファイルに追加された最初のアカウントです。 **pbGlobalProfileSectionGuid** を開くすべての呼び出しは、従来のアカウントExchangeグローバル セクションにリダイレクトされます。 従来以外のユーザー アカウントとやり取りするオブジェクト モデルExchange、従来のユーザー アカウントExchangeします。 
  
レガシ Exchangeサービスには、PR_EMSMDB_LEGACY **(0x3D18000B)** というプロパティが設定されています。これは、メッセージ サービス テーブルで **true** に設定されます。 
  
従来の **emsmdbUID** は、プロファイルの Outlook グローバル プロファイル セクションにも **PidTagExchangeProfileSectionId としてスタンプされます**。 複数の Exchange アカウントをサポートするために記述されたコードは、コードが操作しているアカウントに応じて、正しい **emsmdbUID** を取得する必要がありますので、従来の **emsmdbUID** を取得する必要はありません。
  
## <a name="see-also"></a>関連項目



[複数のアカウントExchange使用する](using-multiple-exchange-accounts.md)


[[�O���[�o�� �v���t�@�C��] �Z�N�V������J�����@](https://support.microsoft.com/kb/188482)

