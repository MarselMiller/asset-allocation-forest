# Asset Allocation Forest

Implementation of the Asset Allocation Forest (AAF) framework proposed by Bettencourt, Tetereva, and Petukhina (2024) for dynamic multi-asset portfolio allocation.

## Project Overview

This project implements a simplified Asset Allocation Forest that combines:

- Random Forest methodology
- Mean-Variance Portfolio Optimization
- Macroeconomic State Variables
- Expanding Window Backtesting

The objective is to dynamically allocate capital across multiple asset classes based on prevailing macroeconomic and financial market conditions.

## Dataset

Period: August 1983 – January 2023

Assets:

- Equity
- Bonds
- Credits
- Commodities
- Gold
- High Yield Bonds

Predictors include:

- Inflation
- Credit Spread
- TED Spread
- CAPE
- Equity Volatility
- Term Spread
- Financial Conditions Indicators

## Methodology

1. Estimate maximum Sharpe Ratio portfolio weights.
2. Evaluate candidate splits using Sharpe Ratio improvement.
3. Build bootstrap allocation trees.
4. Aggregate weights across trees.
5. Perform expanding-window out-of-sample backtesting.

## Results

| Metric | AAF |
|----------|----------:|
| Annual Return | 6.35% |
| Annual Volatility | 7.67% |
| Sharpe Ratio | 0.83 |
| Maximum Drawdown | -18.1% |

## Reference

Bettencourt, L. O., Tetereva, A., & Petukhina, A. (2024).

*Advancing Markowitz: Asset Allocation Forest*
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Asset Allocation Forest

Реализация модели Asset Allocation Forest (AAF), предложенной Bettencourt, Tetereva и Petukhina (2024), для динамического распределения капитала между несколькими классами активов.

## Обзор проекта

В данном проекте реализована упрощённая версия Asset Allocation Forest, объединяющая:

- методологию Random Forest;
- оптимизацию портфеля по критерию максимального коэффициента Шарпа;
- макроэкономические и финансовые факторы;
- out-of-sample тестирование с расширяющимся обучающим окном (expanding window).

Основная цель модели — динамически изменять структуру портфеля в зависимости от текущего состояния экономики и финансовых рынков.

## Данные

Период наблюдений:

```text
Август 1983 — Январь 2023
```

Используемые классы активов:

- Акции (Equity)
- Государственные облигации (Bonds)
- Корпоративные облигации инвестиционного уровня (Credits)
- Товарные активы (Commodities)
- Золото (Gold)
- Высокодоходные облигации (High Yield)

Макроэкономические предикторы включают:

- Инфляцию (Inflation)
- Кредитный спред (Credit Spread)
- TED Spread
- CAPE
- Волатильность рынка акций (Equity Volatility)
- Наклон кривой доходности (Term Spread)
- Индикаторы финансовых условий и другие макроэкономические переменные

## Методология

Алгоритм состоит из следующих этапов:

1. Оптимизация весов портфеля по максимальному коэффициенту Шарпа.
2. Оценка возможных разбиений по улучшению Sharpe Ratio.
3. Построение bootstrap-деревьев распределения активов.
4. Усреднение весов между деревьями.
5. Проведение out-of-sample backtest с использованием expanding window.

## Результаты

| Метрика | Значение |
|----------|----------:|
| Годовая доходность | 6.35% |
| Годовая волатильность | 7.67% |
| Коэффициент Шарпа | 0.83 |
| Максимальная просадка | -18.1% |

## Ограничения реализации

В рамках проекта была реализована упрощённая версия Asset Allocation Forest, состоящая из трёх bootstrap-деревьев. Такое решение было принято для сокращения времени вычислений при проведении полного expanding-window backtest.

Несмотря на это ограничение, модель смогла сформировать устойчивые портфельные веса и обеспечить меньшую максимальную просадку по сравнению с равновзвешенным портфелем.

## Содержимое репозитория

```text
Asset_Allocation_Forest.ipynb   # Основная реализация модели
HW3_MLIF_Report.pdf             # Отчёт по проекту
```

## Использованная статья

Bettencourt, L. O., Tetereva, A., & Petukhina, A. (2024).

*Advancing Markowitz: Asset Allocation Forest*
