---
title: メッセージ ストア プロバイダーの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: eda62a4cd31e0de695d52391a6717e7a0f5ea581
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327208"
---
# <a name="structure-of-message-store-providers"></a>メッセージ ストア プロバイダーの構造
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロバイダーは、メモリで実行されている場合、 [IMSProvider: IUnknown](imsprovideriunknown.md)インターフェイスです。 **IMSProvider**インターフェイスを使用すると、クライアントアプリケーションと MAPI スプーラーがメッセージストアにログオンおよびログオフすることができます。 クライアントアプリケーションと MAPI スプーラーがメッセージストア内のフォルダーおよびメッセージへのアクセスに使用するインターフェイスは、 [IMSLogon](imslogoniunknown.md)および[IMsgStore](imsgstoreimapiprop.md)インターフェイスです。 これらのインターフェイスは、通常、メッセージストアが最初にログオンしたときに作成されますが、メッセージストア DLL の[msproviderinit](msproviderinit.md)エントリポイントで作成することもできます。 
  
**IMSLogon**および**IMsgStore**インターフェイスはいくつかのメソッドを共有するので、これらのインターフェイスの両方から継承する1つのクラスオブジェクトを作成する方が簡単な場合があります。 これらのインターフェイスを個別のオブジェクトに実装し、 **IMSLogon**および**IMsgStore**インターフェイスのメソッドから呼び出すことができる共有メソッドを実装する、DLL に内部でヘルパー関数を記述することもできます。 
  
次の図は、実行中のメッセージストア内のオブジェクト階層の概要を示しています。
  
**メッセージ ストアのオブジェクト階層**
  
![メッセージストアオブジェクトの階層](media/storeobj.gif "メッセージストアオブジェクトの階層")
  
## <a name="see-also"></a>関連項目

- [MAPI メッセージ ストア プロバイダーの開発](developing-a-mapi-message-store-provider.md)

