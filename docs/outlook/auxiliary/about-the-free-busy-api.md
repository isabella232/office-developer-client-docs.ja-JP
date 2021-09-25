---
title: 空き時間情報 API について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: 空き時間情報 API を使用すると、メール プロバイダーは指定した時間範囲内で指定したユーザー アカウントの空き時間情報を提供できます。
ms.openlocfilehash: 9b57a2958298098bda119ae260453f56d7cd1fca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580434"
---
# <a name="about-the-freebusy-api"></a>空き時間情報 API について

空き時間情報 API を使用すると、メール プロバイダーは指定した時間範囲内で指定したユーザー アカウントの空き時間情報を提供できます。 ユーザーの予定表の時間のブロックの空き時間情報の状態は、次の 1 つになります。
  
## <a name="create-a-freebusy-provider"></a>空き時間情報プロバイダーを作成する

メール ユーザーに空き時間情報を提供するために、メール プロバイダーは空き時間情報プロバイダーを作成し、空き時間情報に登録Outlook。 空き時間情報プロバイダーは、次のインターフェイスを実装する必要があります。 これらのインターフェイスのメンバーの数はサポートされていないので、指定した戻り値を返す必要があります。 特に、空き時間情報 API では、空き時間情報への書き込みアクセスとアカウントへのアクセスの委任はサポートされていません。
  
- [IFreeBusySupport](ifreebusysupport.md) —このインターフェイスは、指定されたユーザーの空き時間情報データにアクセスするインターフェイスの仕様をサポートします。 FBUser [を使用して](fbuser.md) ユーザーを識別します。 
    
- [IFreeBusyData](ifreebusydata.md) —このインターフェイスは、特定のユーザーの時間範囲を取得および設定し、この時間範囲内のデータの空き時間情報ブロックを列挙するためのインターフェイスを返します。 相対時間を使用して、この時間範囲を取得および設定します。 詳細については、「相対時間を [使用して空き時間情報にアクセスする」を参照してください](how-to-use-relative-time-to-access-free-busy-data.md)。
    
- [IEnumFBBlock](ienumfbblock.md) —このインターフェイスは、時間範囲内のユーザーのデータの空き時間情報ブロックへのアクセスと列挙をサポートします。 
    
   > [!NOTE]
   > 列挙には、ユーザーの予定表の時間の空き時間状態を示す空き時間情報ブロックが含まれています [(IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)で指定)。 予定表のアイテム (予定や会議出席依頼など) は、列挙のフォーム ブロックです。 予定表で隣接し、同じ空き時間情報の状態を持つアイテムは、1 つのブロックを形成するために結合されます。 予定表の空き時間もブロックを形成します。 したがって、列挙の 2 つの連続するブロックの空き時間情報の状態は同じではありません。 これらのブロックは時間内に重複しません。 予定表に重複するアイテムがある場合、Outlook は、これらのアイテムを結合して、次の優先順位 (アウトオブオフィス、ビジー、暫定的) に基づいて、列挙内の重複しない空き時間情報ブロックを形成します。 
  
空き時間情報プロバイダーを Outlook、メール プロバイダーは次の操作を行う必要があります。
  
1. 空き時間情報プロバイダーを COM に登録し、プロバイダーの **IFreeBusySupport** の実装にアクセスできる CLSID を提供します。 
    
2. システム Outlookに次のキー (バージョンの Outlook を表す) を設定して、空き時間情報プロバイダーが存在することを確認 `<xx.x>` します。 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   たとえば、トランスポート プロバイダーが SMTP の場合、プロバイダーを Microsoft Outlook 2010 に登録するには、次の表のデータに次のキーを設定します。 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |名前 |種類 |値 |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{IFreeBusySupport の各実装の CLSID}  |
   
   このシナリオでは、Outlook COM クラスを共同作成し、それを使用して SMTP メール ユーザーの空き時間情報を取得します。
    
SMTP 以外のアドレス入力タイプを使用するアドレス帳とトランスポート プロバイダーをサポートするには、名前を変更  *します* 。 
  
> [!NOTE]
> インストール中に、空き時間情報プロバイダーは、同じアドレス エントリの種類のレジストリ設定が既に存在するかどうかを確認する必要があります。 その場合、空き時間情報プロバイダーは、そのアドレス エントリの種類の現在のプロバイダーを上書きし、アンインストール時にそのプロバイダーに復元する必要があります。 ただし、ユーザーが同じアドレス エントリの種類に対して複数の空き時間情報プロバイダーをインストールしている場合、ユーザーはこれらのプロバイダーをインストールと逆の順序でアンインストールする必要があります (つまり、常に最新のプロバイダーをアンインストールしてください)。 それ以外の場合、レジストリは既にアンインストールされているプロバイダーを指している可能性があります。 
  
## <a name="api-components"></a>API コンポーネント

空き時間情報 API には、次のコンポーネントが含まれています。
  
### <a name="definitions"></a>定義

- [定数 (空き時間情報 API)](constants-free-busy-api.md)
    
### <a name="data-types"></a>データ型

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>インターフェイス

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    

