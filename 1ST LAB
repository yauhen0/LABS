import java.lang.Math;

public class Sum
{
    public static void main(String[] args)
    {
        try
        {
            if (args.length != 2)
                throw new IllegalArgumentException("Number of arguments aren`t 2");
            if(Double.parseDouble(args[1]) < 0)
                throw new NumberFormatException();

            double res = calculateSum(Double.parseDouble(args[0]),Double.parseDouble(args[1]));
            System.out.println("Result: " + res);
        }
        catch (NumberFormatException e)
        {
            System.out.println("Arguments are incorrect");
            System.exit(0);
        }
        catch (IllegalArgumentException e)
        {
            System.out.println(e);
            System.exit(0);
        }
    }
    public static double Sum(int k ,double x,double precision, double currentTerm)
    {
        if (Math.abs(currentTerm) < precision)
            return 0;

        currentTerm *= -((Math.pow(k + 1, 2) * x) / Math.pow(k + 2, 2));

        return currentTerm +  Sum(++k,x,precision,currentTerm);
    }

    public static double calculateSum(double x,double precision)
    {
        int k = 1;
        double currentTerm = (Math.pow(-1, k) * Math.pow(x, k)) / Math.pow(k + 1, 2);
        return Sum(k,x,precision,currentTerm) + currentTerm;
    }
}
