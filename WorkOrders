select
	*
from
	edw.wo_cmpltd_dly_fact wo
	inner join edw.employee_type_dim empType on
		wo.tech_employee_type_key = empType.employee_type_key
where
	wo.wo_completion_dt_key >= trunc(add_months(sysdate,-12),'year') and
	empType.employee_type_grp = 'Field Tech'
