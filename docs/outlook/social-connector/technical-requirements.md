---
title: 技術的な要件
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: ここでサポートされているプログラミング言語について説明、COM の可視性とメソッドが型の要件、および Outlook ソーシャル コネクタ (OSC) プロバイダーの拡張機能 DLL の詳細を返します。
ms.openlocfilehash: 94b57e20957f3d8d779c4d3324ecbb8ccd37f60a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804460"
---
# <a name="technical-requirements"></a>技術的な要件

ここでサポートされているプログラミング言語について説明、COM の可視性とメソッドが型の要件、および Outlook ソーシャル コネクタ (OSC) プロバイダーの拡張機能 DLL の詳細を返します。 
  
## <a name="programming-language-and-com-requirements"></a>プログラミング言語や COM の要件

Visual C# または Visual Basic では、マネージ言語または Visual C++ などのアンマネージ言語を使用して、OSC プロバイダーを作成できます。 OSC プロバイダーを開発するのには COM 参照可能 DLL コンポーネントを作成できる任意のツールを使用することができます。 プロバイダーを開発するのにはマネージ コードまたはアンマネージ言語を使用するかは、アカウントのダウンロードのサイズとプロバイダーのインストール パッケージの依存関係になりません。
  
OSC プロバイダーは、次のように定義されている COM 参照可能である必要があります。
  
- インストールが完了したら、COM 登録または regsvr32 を使用して、OSC プロバイダーを登録してください。
    
- OSC プロバイダー DLL の COM 登録は、HKCU または HKLM の下のプロバイダーを登録します。 
    
- プロバイダーの ProgID が登録されている`HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`。
    
- マネージ言語で開発された、OSC プロバイダーは、COM 参照可能です。
    
- OSC プロバイダーは、プロバイダーの DLL には、シングル スレッド アパートメント (STA) とマルチ スレッド アパートメント (MTA) スレッド モデルの両方がサポートしていることを示す Windows のレジストリに値を追加する必要があります。 COM スレッド モデルの詳細については、[説明および動作の OLE のスレッド化モデル](http://support.microsoft.com/kb/150777)を参照してください。
    
OSC プロバイダーの拡張機能のメソッドは、**文字列**または**ブール値**などのプリミティブ型を返す必要があります。 特定の**文字列**では、OSC プロバイダーの拡張機能のスキーマ定義に従うものと値を返します。 戻り値として XML のみがサポートされています。 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>OSC プロバイダーの拡張機能 DLL の詳細

OSC プロバイダーの拡張機能をサポートしているコンポーネントは、OSC プロバイダーの拡張機能 DLL です。 サード パーティの開発者は、これらの機能拡張インターフェイスを使用して、OSC プロバイダー Dll を作成できます。 OSC プロバイダーの拡張機能 DLL の詳細を次に示します。
  
- 拡張機能 DLL のファイル名: socialprovider.dll
    
- 拡張機能 DLL のフレンドリ名: Microsoft Outlook のイベント プロバイダーの拡張性
    
- 拡張機能 DLL のメジャー バージョン: 15.0
    
- Extensibiilty DLL のタイプ ライブラリのバージョン: 1.1
    
## <a name="miscellaneous-technical-information"></a>その他の技術情報

OSC プロバイダーの機能拡張モデルでは、JavaScript オブジェクト表記法 (JSON) はサポートされていません。
  
XML パーサーでは、依存関係はありません。 OSC プロバイダー Office、Microsoft XML Core Services (MSXML) などに含まれている XML パーサーを使用して、Microsoft.NET Framework に組み込まれた機能を解析中の XML を使用したり、サード パーティ製の XML パーサーを使用できます。 
  
## <a name="see-also"></a>関連項目

- [プロバイダーを開発するためのベスト プラクティス](best-practices-for-developing-a-provider.md)  
- [プロバイダーを開発する学習のためのクイック ステップ](quick-steps-for-learning-to-develop-a-provider.md)
- [プロバイダーを展開します。](deploying-a-provider.md)  
- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

