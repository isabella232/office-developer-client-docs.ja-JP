---
title: InfoPath を別のアプリケーションで XML エディターとしてホストする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: により、開発者は InfoPath のフォーム編集環境を基幹業務アプリケーションを統合するためにカスタムの Windows アプリケーションで Microsoft InfoPath のフォーム編集環境をホストすることができます。
ms.openlocfilehash: dd87cba7219b5647bd2b20dd67c6eb0f1811cc59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799103"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>InfoPath を別のアプリケーションで XML エディターとしてホストする

Microsoft InfoPath フォームの編集環境は、カスタムの Windows アプリケーションでホストできます。開発者はこの機能を利用して、InfoPath フォームの編集環境を基幹業務アプリケーションに統合できます。従来型 COM ベース アプリケーションの開発者は、IPEDITOR.DLL を参照する方法で **InfoPathEditorObject** オブジェクトを使用できます。Microsoft .NET ベース アプリケーションの開発者は、COM インターフェイスに基づくマネージ型を提供する **Microsoft.Office.InfoPath.FormControl** アセンブリを使用できます。IPEDITOR.DLL および **Microsoft.Office.InfoPath.FormControl** アセンブリは両方とも InfoPath と一緒に C:\Program Files\Microsoft Office\Office15 または C:\Program Files (x86)\Microsoft Office\Office15 フォルダーにインストールされます。 
  
カスタムの Windows フォーム アプリケーションで InfoPath 2007 フォーム編集環境をホストしている、MSDN の記事では、 **FormControl**オブジェクトとを独自に組み込む方法に焦点を当てます。.NET ベースのアプリケーションです。 この記事に関連するダウンロード パッケージには、InfoPath フォームの編集環境を COM **IOleCommandTargets** を使用して再現する .NET 関数を提供するカスタム アプリケーションが収録されています。
  

