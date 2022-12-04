#Вариант 11


from pulp import *

x1=pulp.LpVariable("x1", lowBound=0)
x2=pulp.LpVariable("x2", lowBound=0)
x3=pulp.LpVariable("x3", lowBound=0)
x4=pulp.LpVariable("x4", lowBound=0)
x5=pulp.LpVariable("x5", lowBound=0)
x6=pulp.LpVariable("x6", lowBound=0)
x7=pulp.LpVariable("x7", lowBound=0)
x8=pulp.LpVariable("x8", lowBound=0)
x9=pulp.LpVariable("x9", lowBound=0)
x10=pulp.LpVariable("x10", lowBound=0)
x11=pulp.LpVariable("x11", lowBound=0)
x12=pulp.LpVariable("x12", lowBound=0)
x13=pulp.LpVariable("x13", lowBound=0)
x14=pulp.LpVariable("x14", lowBound=0)
x15=pulp.LpVariable("x15", lowBound=0)
x16=pulp.LpVariable("x16", lowBound=0)
x17=pulp.LpVariable("x17", lowBound=0)
x18=pulp.LpVariable("x18", lowBound=0)
x19=pulp.LpVariable("x19", lowBound=0)
x20=pulp.LpVariable("x20", lowBound=0)
x21=pulp.LpVariable("x921", lowBound=0)
x22=pulp.LpVariable("x22", lowBound=0)
x23=pulp.LpVariable("x23", lowBound=0)
x24=pulp.LpVariable("x24", lowBound=0)
x25=pulp.LpVariable("x25", lowBound=0)


problem = pulp.LpProblem("0", LpMaximize)
problem += -3*x1-4*x2-3*x3-1*x4-5*x5-2*x6-3*x7-5*x8-0*x9-8*x10-1*x11-2*x12-3*x13-3*x14-4*x15-4*x16-5*x17-7*x18-9*x19-9*x20-5*x21-6*x22-8*x23-4*x24-7*x25, "Функция цели"
problem += x1+x2+x3+x4+x5 <= 300 #поставщик
problem += x6+x7+x8+x9+x10 <= 200 #поставщик
problem += x11+x12+x13+x14+x15 <= 300 #поставщик
problem += x16+x17+x18+x19+x20 <= 100 #поставщик
problem += x21+x22+x23+x24+x25 <= 400 #поставщик


problem += x1+x6+x11+x16+x21 == 300 #потребитель
problem += x2+x7+x12+x17+x22 == 200 #потребитель
problem += x3+x8+x13+x18+x23 == 100 #потребитель
problem += x4+x9+x14+x19+x24 == 200 #потребитель
problem += x5+x10+x15+x20+x25 == 300 #потребитель



problem.solve()
print("Result: ")
for variable in problem.variables():
  print(variable.name , " = ", variable.varValue)
print("Стоимость доставки: ")
print(abs(value(problem.objective)))
