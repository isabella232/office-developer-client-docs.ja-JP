---
title: 空き/予約済み API について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: 空き/予約済み API では、指定の時間範囲内の指定したユーザー アカウントの空き時間情報のステータス情報を提供するメール プロバイダーを使用します。
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799300"
---
# <a name="about-the-freebusy-api"></a>空き/予約済み API について

空き/予約済み API では、指定の時間範囲内の指定したユーザー アカウントの空き時間情報のステータス情報を提供するメール プロバイダーを使用します。 ユーザーの予定表で時間帯の空き時間情報のステータスは、次のいずれか: 不在時の使用中、仮承諾、または無料です。
  
## <a name="create-a-freebusy-provider"></a>空き/予約済みのプロバイダーを作成します。

メール ユーザーに空き時間情報を提供するには、メール プロバイダーは空き/予約済みのプロバイダーを作成し、Outlook に登録します。 空き/予約済みのプロバイダーは、次のインタ フェースを実装しなければなりません。 これらのインターフェイスのメンバーの多くがサポートされておらず、指定した戻り値を返す必要があることに注意してください。 具体的には、空き/予約済み API は空き時間情報およびアカウントへのアクセスを委任への書き込みアクセスをサポートしていません。
  
- [IFreeBusySupport](ifreebusysupport.md) -このインターフェイスは、指定したユーザーの空き時間情報データにアクセスするインターフェイスの仕様をサポートしています。 [FBUser](fbuser.md)を使用してユーザーを識別します。 
    
- [IFreeBusyData](ifreebusydata.md) -このインターフェイスを取得しユーザーが指定した時間範囲を設定し、この時間の範囲内のデータのブロックの空き時間情報を列挙するためのインターフェイスを返します。 相対時間を使用して取得し、この時間範囲を設定します。 詳細については、[空き時間情報データにアクセスするのには相対的な時間の使用](how-to-use-relative-time-to-access-free-busy-data.md)を参照してください。
    
- [IEnumFBBlock](ienumfbblock.md) -このインターフェイスにアクセスして、時間の範囲内でのユーザーのデータのブロックの空き時間情報を列挙をサポートしています。 
    
   > [!NOTE]
   > 列挙体には、( [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)で指定された) 時間の範囲内で、ユーザーの予定表で時間の期間の空き時間情報のステータスを示す空き時間情報のブロックが含まれています。 予定および会議出席依頼などの予定表のアイテムは、列挙体のブロックを形成します。 カレンダーに互いに隣接しているし、同じ空き時間情報のステータスを持つアイテムは、1 つのブロックを 1 つのフォームに結合されます。 カレンダー上の時間の無料期間もブロックを形成します。 したがって、列挙型の連続する 2 つのブロックがありません。 には、同じ空き時間情報のステータスがあります。 これらのブロックは、時に重複しません。 これらの項目の優先順位に基づいて列挙体の空き/予約済みブロックの重複を形成する結合 Outlook の予定表に重複する項目がある場合は、: 不在時の予定あり、仮の予定です。 
  
Outlook で空き時間情報のプロバイダーを登録するにメール プロバイダーは、次の操作を行う必要があります。
  
1. COM、 **IFreeBusySupport**のプロバイダーの実装にアクセスできるようにするための CLSID を提供することで、空き/予約済みのプロバイダーを登録します。 
    
2. 自動的に次のキーを設定することによって、空き/予約済みのプロバイダーの存在を (位置`<xx.x>`Outlook のバージョンを表します)、システム レジストリに。 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   などのトランスポート プロバイダーが SMTP である場合は、Microsoft Outlook 2010 では、プロバイダーを登録するのには次のキーに設定次の表のデータ。 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |名前 |種類 |値 |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{CLSID} IFreeBusySupport のそれぞれの実装について  |
   
   このシナリオでは、Outlook の COM クラスを再作成して使用して SMTP メール ユーザーの空き時間情報を取得します。
    
SMTP 以外のアドレス エントリの種類を使用しているアドレス帳とトランスポート プロバイダーをサポートするためには、それに応じて*名前*を変更します。 
  
> [!NOTE]
> かどうかのレジストリ設定、インストール時にプロバイダーの空き時間情報をチェック、同じアドレスのエントリの種類が既に存在します。 場合は、空き/予約済みのプロバイダーはそのアドレスのエントリの種類の現在のプロバイダーを上書きし、そのプロバイダーのアンインストール時に復元ください。 ただし、ユーザーが同じアドレスのエントリの種類の 1 つ以上の空き/予約済みのプロバイダーをインストールしている場合、ユーザーする必要がありますアンインストールこれらのプロバイダーのインストールと逆の順序で (つまり、常にアンインストール、最新のプロバイダー)。 それ以外の場合、レジストリは、既にアンインストールされているプロバイダーにポイントがあります。 
  
## <a name="api-components"></a>API コンポーネント

空き/予約済みの API には、次のコンポーネントが含まれています。
  
### <a name="definitions"></a>定義

- [定数 (空き時間情報の API)](constants-free-busy-api.md)
    
### <a name="data-types"></a>データ型

- [FBBlock_1](fbblock_1.md)
- [FBStatus](fbstatus.md)
- [FBUser](fbuser.md)
    
### <a name="interfaces"></a>インターフェイス

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData](ifreebusydata.md)
- [IFreeBusySupport](ifreebusysupport.md)
    

