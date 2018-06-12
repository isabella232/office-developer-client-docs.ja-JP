---
title: �C�x���g�̏���
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798877"
---
# <a name="handling-events"></a>�C�x���g�̏���

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Excel 2010 �ȍ~�� XLL �́A�񓯊��֐��̃��C�t �T�C�N����Ǘ����邽�߂ɐ݌v���ꂽ�C�x���g���M�ł��܂��B���̃C�x���g�͎��̂Ƃ���ł��B
  
- **CalculationEnded**:Excel �̌v�Z���I�������Ƃ��ɔ������܂��B�v�Z���Ɋ��蓖�Ă����\�[�X�́A���̃C�x���g�̌�ŉ���ł��܂��B
    
- **CalculationCanceled**:���[�U�[���v�Z�𒆒f�����Ƃ��ɔ������܂��BXLL �́A������񓯊��̃A�N�e�B�r�e�B���~���܂��B���̃C�x���g�̒���ɁA **CalculationEnded** �C�x���g���������܂��B 
    
�����̃C�x���g��������邽�߂ɁAXLL �ł� C API �֐��� [xlEventRegister](xleventregister.md) ��g�p���܂��B 
  
> [!NOTE]
> [!����] **CalculationEnded** �� **CalculationCanceled** �́A�v���O�����ɂ��Čv�Z���ɂ͔������܂���B 
  

