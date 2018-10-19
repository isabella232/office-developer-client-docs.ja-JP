---
title: Office Developer Tools for Visual Studio で提供される信頼できるアプリケーション オブジェクトを使用する
TOCTitle: Using a trusted application object provided by Office Developer Tools for Visual Studio
ms:assetid: 3778122f-f60e-48e7-8e72-f3aef168bae2
ms:mtpsurl: https://msdn.microsoft.com/library/Bb622502(v=office.15)
ms:contentKeyID: 55119787
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 7b56e59b19f1c9a0ee4c730f14200c3e501f5290
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406114"
---
# <a name="using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio"></a>Office Developer Tools for Visual Studio で提供される信頼できるアプリケーション オブジェクトを使用する

Office Developer Tools for Visual Studio を使用して管理対象アドインを開発する場合は、常に、Visual Studio が提供する [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) オブジェクトを使用します。 

Outlook の新しいインスタンスを自動化することを目的としていない場合は、Outlook の新しいインスタンスを作成するために New または new キーワードを使用しないでください。その理由は、この **Application** オブジェクトのインスタンスが、Outlook のオブジェクト モデル ガードの観点からは信頼されていないためです。 

アドインで **Application** オブジェクトの信頼されていないインスタンスを使用すると、クライアントが実行している Outlook のバージョンによっては、そのアドインが既定でオブジェクト モデルのいくつかのメンバーで Outlook のオブジェクト モデル ガードを呼び出すようになります。 

オブジェクト モデル ガードの動作に関する詳細については、「[Outlook 2007 でのコード セキュリティの変更点](https://msdn.microsoft.com/library/bb226709\(v=office.15\))」を参照してください。 「Outlook 2007 でのコード セキュリティの変更点」の記事では既定で信頼されている COM アドインについて記述されていても、このデザインは Outlook 2007 以降の Outlook バージョンに適用されるものであり、信頼は同じ方法で管理対象アドインにも適用される点に注意してください。 アドインが管理対象かどうかにかかわらず、信頼は、そのアドインが信頼された **Application** オブジェクトを使用するという前提に基づきます。

