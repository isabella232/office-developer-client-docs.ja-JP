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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316430"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>PidTagExchangeProfileSectionId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
複数の Microsoft Exchange Server アカウントを使用している場合にアカウントを判別するために使用される動的に生成される GUID を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|識別子:  <br/> |0x3d150102  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |複数の Exchange アカウント  <br/> |
   
## <a name="remarks"></a>解説

microsoft outlook 2010 および microsoft outlook 2013 は、1つの exchange アカウントではなく複数の exchange アカウントをサポートしています。 複数の Exchange アカウントに対応するために、MAPI プロファイルレイアウトが変更されました。 Microsoft Office Outlook 2007 以前では、プロファイルには、サーバー名、ユーザー名、オフラインフォルダーファイル (.ost) などの Exchange 設定専用の固定プロファイルセクションが含まれていました。 位置. これらの設定は、一意の識別子で**pbGlobalProfileSectionGuid**プロパティを使用して識別されました。 exchange の設定に使用されるセクションは、「exchange グローバルプロファイル」セクションと呼ばれます。 
  
固定プロファイルセクションの場所は、複数の Exchange アカウントに対応するのに十分ではなくなりました。 代わりに、プロファイル内の Exchange アカウントごとに、そのアカウントの設定専用のセクションが存在します。 Exchange の設定に使用される新しいセクションは、一意の識別子**emsmdbUID**によって識別されます。
  
Exchange アカウントの [メッセージサービスプロファイル] セクションでは、アカウントの作成時に動的に生成される GUID を含むプロパティを見つけることができます。 この GUID は、 **PidTagExchangeProfileSectionId**プロパティに格納されます。 メッセージストアとアドレス帳コンテナーは、どの Exchange アカウントが属しているかを判断するためのプロパティを公開します。 メッセージサービステーブルでアクセスできるようになると、各 Exchange サービスはこのプロパティを公開します。 
  
このプロパティは、次のいずれかのインターフェイスに対してクエリを実行した後に、 **PidTagExchangeProfileSectionId**上の[imapiprop:: GetProps](imapiprop-getprops.md)への呼び出しによって取得できます。 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
オブジェクトが Exchange に関連付けられていない場合、呼び出しは**MAPI_E_NOT_FOUND**を返します。
  
アドレス帳を表示するときに、 **PidTagExchangeProfileSectionId**のコンテナーを制限することができます。 コンテナーを開いた後、そのコンテナーから**emsmdbUID**を照会することができます。 また、受信者が Exchange アドレス帳から選択されている場合は、受信者の**PidTagExchangeProfileSectionId**もプロパティの一覧に表示されることに注意してください。 
  
> [!NOTE]
> コードサンプルと関数ヘッダー全体で、この GUID は**emsmdbUID**と呼ばれます。 
  
exchange アカウントの1つは、従来の exchange アカウントとしてマークされています。 通常、これはプロファイルに最初に追加されるアカウントです。 open **pbGlobalProfileSectionGuid**へのすべての呼び出しは、従来のアカウントの Exchange グローバルセクションにリダイレクトされます。 従来の exchange アカウントではないオブジェクトモデル呼び出しは、従来の exchange アカウントとも対話します。 
  
従来の Exchange サービスには、 **PR_EMSMDB_LEGACY** (0x3D18000B) というプロパティがあり、メッセージサービステーブルでは**true**に設定されています。 
  
従来の**emsmdbUID**も、プロファイルの Outlook グローバルプロファイルセクションに**PidTagExchangeProfileSectionId**としてスタンプされます。 複数の Exchange アカウントをサポートするように記述されたコードは、コードが対話するアカウントに応じて正しい**emsmdbUID**を取得する必要があるため、従来の**emsmdbUID**を取得する必要はありません。
  
## <a name="see-also"></a>関連項目



[複数の Exchange アカウントの使用](using-multiple-exchange-accounts.md)


[[�O���[�o�� �v���t�@�C��] �Z�N�V������J�����@](https://support.microsoft.com/kb/188482)

