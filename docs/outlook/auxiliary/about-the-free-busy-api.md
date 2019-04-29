---
title: 空き時間情報 API について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: 空き時間情報 API を使用すると、指定したユーザーアカウントに対して、指定した時間範囲内に、メールプロバイダーが空き時間情報の状態情報を提供できます。
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433760"
---
# <a name="about-the-freebusy-api"></a>空き時間情報 API について

空き時間情報 API を使用すると、指定したユーザーアカウントに対して、指定した時間範囲内に、メールプロバイダーが空き時間情報の状態情報を提供できます。 ユーザーの予定表の時間ブロックの空き時間情報は、不在時、取り込み中、仮承諾、または無料のいずれかの状態になります。
  
## <a name="create-a-freebusy-provider"></a>空き時間情報プロバイダーを作成する

メールユーザーに空き時間情報を提供するために、メールプロバイダーは空き時間情報プロバイダーを作成し、それを Outlook に登録します。 空き時間情報プロバイダーは、次のインターフェイスを実装する必要があります。 これらのインターフェイスのメンバーの数はサポートされておらず、指定された戻り値を返す必要があることに注意してください。 特に、空き時間情報 API は、空き時間情報への書き込みアクセス、およびアカウントへの代理人アクセスをサポートしていません。
  
- [IFreeBusySupport](ifreebusysupport.md) —このインターフェイスは、指定されたユーザーの空き時間情報データにアクセスするインターフェイスの指定をサポートしています。 [fbuser](fbuser.md)を使用してユーザーを識別します。 
    
- [IFreeBusyData](ifreebusydata.md) —このインターフェイスは、指定されたユーザーの時間範囲を取得および設定し、この時間範囲内のデータの空き時間情報ブロックを列挙するためのインターフェイスを返します。 この時間範囲を取得して設定するには、相対時間を使用します。 詳細については、「[相対時間を使用して空き時間情報データにアクセスする](how-to-use-relative-time-to-access-free-busy-data.md)」を参照してください。
    
- [IEnumFBBlock](ienumfbblock.md) —このインターフェイスは、時間範囲内のユーザーのデータの空き時間情報ブロックへのアクセスと列挙をサポートしています。 
    
   > [!NOTE]
   > 列挙体には、時間範囲 ( [IFreeBusyData:: enumblocks](ifreebusydata-enumblocks.md)で指定されます) 内のユーザーの予定表の空き時間状態を示す空き時間情報ブロックが含まれます。 予定や会議出席依頼などの予定表のアイテムには、列挙のフォームブロックが含まれます。 予定表で相互に隣接していて、空き時間情報の状態が同じであるアイテムは、1つのブロックを形成するために結合されます。 予定表の空き時間もブロックを形成します。 そのため、列挙内の2つの連続するブロックの空き時間状態は同じではありません。 これらのブロックは時間内に重なりません。 予定表に重複するアイテムがある場合、Outlook はこれらのアイテムを結合して、この優先順位 (不在、取り込み中、仮承諾) に基づいて列挙で重複しない空き時間ブロックを形成します。 
  
空き時間情報プロバイダーを Outlook に登録するには、メールプロバイダーは次の操作を実行する必要があります。
  
1. プロバイダーの**IFreeBusySupport**の実装へのアクセスを許可する CLSID を提供して、空き時間情報プロバイダーを COM に登録します。 
    
2. システムレジストリ内の次のキー (outlook のバージョンを表す場所`<xx.x>` ) を設定して、空き時間情報プロバイダーが存在することを Outlook に認識させます。 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   たとえば、トランスポートプロバイダーが SMTP の場合、プロバイダーを Microsoft Outlook 2010 に登録するには、次のキーを次の表のデータに設定します。 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |名前 |種類 |値 |
   |:-----|:-----|:-----|
   |SMTP  |REG_SZ  |{IFreeBusySupport の各実装の CLSID  |
   
   このシナリオでは、Outlook は COM クラスを共同作成し、それを使用して任意の SMTP メールユーザーの空き時間情報を取得します。
    
SMTP 以外のアドレスエントリの種類を使用するアドレス帳とトランスポートプロバイダーをサポートするには、その*名前*を適宜変更します。 
  
> [!NOTE]
> インストール時に、空き時間情報プロバイダーは、同じアドレスエントリの種類のレジストリ設定が既に存在するかどうかを確認する必要があります。 その場合は、そのアドレスエントリの種類について現在のプロバイダーを空き時間情報プロバイダーが上書きし、アンインストール時にそのプロバイダーに復元する必要があります。 ただし、ユーザーが同じアドレスエントリの種類に対して複数の空き時間情報プロバイダーをインストールしている場合は、これらのプロバイダーをインストールとは逆の順序でアンインストールする必要があります (つまり、常に最新のプロバイダーをアンインストールする必要があります)。 それ以外の場合は、既にアンインストールされているプロバイダーをレジストリが参照している可能性があります。 
  
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
    

